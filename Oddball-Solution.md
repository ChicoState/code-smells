public class LoadUserProfileAction extends Action{
  .
  .
  . 
  return process("ViewAction");
}

public class UploadAction extends Action{
  .
  .
  . 
  return process("ViewAction");
}

public class ShowLoginAction extends Action{
  .
  .
  . 
  return viewAction();
}

This is harmful because it makes one solution different from the others used and so it has to be handled differently.
It should be fixed by changing the code to match the form of the other solutions.
To recognize this smell, look for a single solution that is formatted differently that the others.
