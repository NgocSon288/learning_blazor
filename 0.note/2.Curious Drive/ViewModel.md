# Note

## Implicit

   <!--
      class ProfileViewModel{
         string Name {get;set;}

         public static implicit  operator ProfileViewModel(User user){
            return new  ProfileViewModel(){
               Name = user.Name;
            }
         }

         public static implicit  operator User(ProfileViewModel profileViewModel){
            return new  User(){
               Name = profileViewModel.Name;
            }
         }
      }
   -->
