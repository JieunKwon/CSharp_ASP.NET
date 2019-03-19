# CSharp_ASP.NET

ASP.NET Web Forms
-----------------


@Page Directive
-------

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
