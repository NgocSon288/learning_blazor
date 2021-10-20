# Note

-  Sử dụng thư viện WebUtilities để tạo ra đối tượng query string đơn giản hơn
   <!--
      Microsoft.AspNetCore.WebUtilities

      var queryStringParam = new Dictionary<string,string>(){
         ["pageNumber"] = Page.Size
      }

      string url = QueryHelpers.AddQueryString("/api/tasks/", queryStringParam);
   -->

-  Sử dụng thư viện LocalStorage của Blazor
    <!--
       Blazored.LocalStorage
   
       https://github.com/Blazored/LocalStorage
    -->

-  Sử dụng Components.Authorization để đăng nhập
   <!--
      Microsoft.AspNetCore.Components.Authorization

   -->

# Get data

-  Dùng đối tượng [HttpClient] để lấy dữ liệu từ Api

   <!-- await _httpClient.GetFromJsonAsync<AppUser>("/api/AppUsers/1") -->
