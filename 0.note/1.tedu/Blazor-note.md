# Note

-  Các services của blazor sẽ được khai báo trực tiếp trong Program
   <!-- builder.Services.AddTransient<ITaskApiClient, TaskApiClient>() -->

-  Tedu
    <!-- https://github.com/teduinternational/TodoListBlazorWasm -->

# Template

-  Sự kiện click cho phần tử, là một thuộc tính
    <!-- @onclick="()  => OnClickA(1)" -->

-  Kiểm tra đăng nhập của user
   <!--
      <AuthorizeView>
         <Authorized>
            // đã đăng nhập
         </Authorized>
         <NotAuthorized>
            // chưa đăng nhập
         </NotAuthorized>
      </AuthorizeView>
   -->

# Code

-  Hàm khởi tạo trước khi tạo ra Component
   <!-- OnInitializedAsync -->
