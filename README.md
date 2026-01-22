# .
  brew install dotnet@8                                                                                                                                                                       
dotnet new mvc -n YourProjectName -au Individual -f net8.0                                                                                                                                  
                                                                                                                                                                                              
  Пакеты EF Core:                                                                                                                                                                             
                                                                                                                                                                                              
  dotnet add package Microsoft.EntityFrameworkCore.SqlServer --version 8.0.* && \                                                                                                             
  dotnet add package Microsoft.EntityFrameworkCore.Tools --version 8.0.* && \                                                                                                                 
  dotnet add package Microsoft.EntityFrameworkCore.Design --version 8.0.*        


  dotnet ef migrations add InitialCreate                                                                                                                                                      
  dotnet ef database update
