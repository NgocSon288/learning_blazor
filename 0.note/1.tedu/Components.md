# Blazor Component

-  Thông bào state thay đổi để render lại. Phương thức có sẵn của Component
    <!-- StateHasChanged() -->
-  Đặt tên biến cho một conponent nào đó, để có thể gọi trong code cs.
   <!-- @ref="EleConfirm" -->

## [EditForm]

-  Model="Item"
-  Event

   -  Luôn luôn Submit
      <!-- OnSubmit="OnSubmitForm" -->
   -  Khi Form hợp lệ mới Submit
       <!-- OnValidSubmit="OnValidSubmitForm" -->
   -  Khi Form không hợp lệ mới Submit
       <!-- OnInValidSubmit="OnInValidSubmitForm" -->

### [Validate]

-  Để cho biết form nào đang dùng hiển thị lỗi
   <DataAnnotationValidator>
-  Hiển thị tất cả các lỗi
   <ValidationSumary/>

-  Hiển thị lỗi cho một lỗi nào đó, \>\> Hiển thị ErrorMessage
   <ValidationMessage For="()=>Item.Name">

### InputText

-  @bind-Value="Item.Id"

### InputSelect

-  @bind-Value="Item.List"

*  Cố thể dùng <option> bên trong Input

## Tham số

-  Các Component có thể nhận dữ liệu truyền vào bằng các khai báo thuộc tính và có thêm chỉ thị thuộc tính là [Parameter] trong phần code

   <!--
      [Parameter]
      public Priority Priority {get;set;}
   -->

-  Tham số là Event, khi ta muốn chia ra Component nhỏ xử lý gì đó, sau đó thông báo ra cho cha biết đã xử lý, và có thể truyền dữ liệu gì đó ra cho cha. Giống [React]

   -  Con: nhận 1 [parameter], nhận là [EventCallback], trả về [PersonResult]
   <!--
      [Parameter]
      public EventCallback<PersonResult> OnSearchForm{get;set;}

      await ObSearchForm.InvokeAsync(personResult1)
   -->

   -  Cha: truyền vào con bằng Hàm tên [OnSearchForm]
   <!--
      <TaskSearch OnSearchForm="SearchTaskMethod">

      </TaskSearch>


      public async Task SearchTaskMethod(Person personResult){
         // cập nhật dữ liệu gì đó
      }
   -->
