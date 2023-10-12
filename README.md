# BlazorApp.HotReload

This project is designed to highlight the performance issues of the Hot-Reload function in a Blazor application within Visual Studio. 
A critical factor for this performance is the number of Razor components incorporated in the project.

For demonstration purposes, various RazorClassLibrary_* have been provided in this project (based on the standard template):

RazorClassLibrary_500 with 500 Components
RazorClassLibrary_1000 with 1000 Components
RazorClassLibrary_2000 with 2000 Components
When one or more of these projects are referenced, the hot-reload time for a minor change can significantly increase. In my tests, I've observed wait times of up to 50 seconds. It's crucial to emphasize that changes are NOT being made in the referenced projects but only in files like "Home.razor".

Using dotnet watch or JetBrains' Rider, changes are accepted in less than 2 seconds.

These observations suggest that there's room for optimization for the Hot-Reload feature in Visual Studio.