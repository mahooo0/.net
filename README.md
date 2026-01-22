  brew install dotnet@8                                                                                                                                                                       
                                                                                                                                                                                              
  dotnet new mvc -n MyProject -au Individual -f net8.0                                                                                                                                        
  cd MyProject                                                                                                                                                                                
                                                                                                                                                                                              
  dotnet add package Microsoft.EntityFrameworkCore.SqlServer --version 8.0.* && \                                                                                                             
  dotnet add package Microsoft.EntityFrameworkCore.Tools --version 8.0.* && \                                                                                                                 
  dotnet add package Microsoft.EntityFrameworkCore.Design --version 8.0.*                                                                                                                     
                                                                                                                                                                                              
  dotnet add package Microsoft.VisualStudio.Web.CodeGeneration.Design --version 8.0.*                                                                                                         
                                                                                                                                                                                              
  dotnet tool install dotnet-aspnet-codegenerator --version 8.0.* --local                                                                                                                     
                                                                                                                                                                                              
  # 6. Создать модель (Models/Product.cs - вручную)                                                                                                                                           
                                                                                                                                                                                              
  # 7. Добавить DbSet в Data/ApplicationDbContext.cs:                                                                                                                                         
  #    public DbSet<Product> Products { get; set; }                                                                                                                                           
       <a class="nav-link" asp-controller="Products" asp-action="Index">Products</a>                                                                                                                                                                                                                                                                                                       
  dotnet ef migrations add AddProduct                                                                                                                                                         
  dotnet ef database update                                                                                                                                                                   
                                                                                                                                                                                              
  dotnet aspnet-codegenerator controller \                                                                                                                                                    
    -name ProductsController \                                                                                                                                                                
    -m Product \                                                                                                                                                                              
    -dc ApplicationDbContext \                                                                                                                                                                
    --relativeFolderPath Controllers \                                                                                                                                                        
    --useDefaultLayout \                                                                                                                                                                      
    --referenceScriptLibraries                                                                                                                                                                
                                                                                                                                                                                              
  dotnet run
