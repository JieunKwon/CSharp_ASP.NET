# CSharp_ASP.NET

ASP.NET Web Forms
-----------------

Web Application Elements

 Web forms (*.aspx files)

 Master pages (.master files)

 Web Services (*.asmx files or *.svc files)

 Code behind files (*.cs files for C#)

 One or more Web.config the configuration of the application

 Global.asax (global application elements)

 Other components: custom controls, modules, handlers

 Other static resources: HTML / CSS files, images, audio-video files etc


ASP.NET Page
---------

A file with extension *.aspx that resides on a web server and contains:

 Processing instructions for the server

 HTML

 Web Form containing web controls

 Managed code in any language supported by the .NET Framework

 Client-side scripting

 Rendered by the web server in HTML so it can be displayed in any browser


@Page Directive
-------
Every ASP.NET page uses the @Page directive to specify

  - specification the page properties 
  - configuration information for the page 
  - instructions for how to process the page 

        <%@ Page Title="Welcome" Language="C#" MasterPageFile="~/Site.Master" AutoEventWireup="true" CodeBehind="Default.aspx.cs" Inherits="ProjectName._Default" %>


Web Server Controls
--------

Web server controls are similar to HTML buttons and input elements. However, they are processed on the server, allowing you to use server code to set their properties. These controls also raise events that you can handle in server code.

 - starts with an [asp:] prefix
 - runat="server" attribute 
 - ID attribute for reference
 
        <asp:Image  ID="Image1" runat="server" ImageUrl="~/Images/logo.jpg" BorderStyle="None" />

Master Page
-------

A single master page defines the look and feel and standard behavior for all of the pages

    (Site.Master)
    <%@ Master Language="C#" AutoEventWireup="true" CodeBehind="Site.master.cs" Inherits="Project.SiteMaster" %>


To add new page based on master page, select the option of 'Web Form with Master Page' 

    <%@ Page Title="" Language="C#" MasterPageFile="~/Site.Master" AutoEventWireup="true" CodeBehind="MyPage.aspx.cs" Inherits="Project.MyPage" %>
    
    <asp:Content ID="Content1" ContentPlaceHolderID="MainContent" runat="server"> <!-- Content Part --> </asp:Content>


web.config -appSettings 
------------------

An XML file that defines the configuration information for the ASP.NET files in the same folder and any subfolder

Used to store application – settings in the form of key value pairs 

Inside the <appSettings> use the <add> tag with two attributes

-key: stores the key used to access the setting

-value: stores the value associated with the key

In code use the WebConfigurationManager.AppSettings property like a dictionary
  
 
< Three main sections > 

- <appSettings>: used to store custom application settings

- <connectionStrings>: used to store database connection strings

- <system.web>: used to store web configuration sections

  
< compilation settings > 

- runtime settings

- security and encryption settings

- error handling

- session state

- page-level configuration settings

- web control settings

- web services settings

- tracing configuration

  
Application File: global.asax
---------

Contains application level event handlers, global directives and global object tags

Used to perform application initialization, cleanup, logging, profiling and troubleshooting

    <%@ Application Codebehind="Global.asax.cs" Inherits="WebArchitect.Gobal" Language="C#" %>
    

 < Global events > 
 
-Application_Start / Application_End

-Session_Start / Session_End

-Application_Error: invoked whenever an unhandled exception occurs in the application





