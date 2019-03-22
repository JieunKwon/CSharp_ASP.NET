# CSharp_ASP.NET

ASP.NET Web Forms
-----------------

Web Application Elements
 A web application is made of
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

 A file with extension *.aspx that resides on a web server and
contains:
 Processing instructions for the server
 HTML
 Web Form containing web controls
 Managed code in any language supported by the .NET Framework
 Client-side scripting
 Rendered by the web server in HTML so it can be displayed in any
browser


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

