# ZPF_Basics
Basics for .Net ( .Net Standard 2.1 )

## Features
 * Delphi like TIniFile (ini file management)
 * Delphi like TStrings (list of strings)
 * ObjectExtensions
 * StringExtensions
 * BaseViewModel class for an basic MVVM (Model View ViewModel) implemention
 * ...

## Roadmap
[ ] ...


## Changelog  
### Version 2.1.1.3 - 08/03/2025
* Downgrade to .Net Standard 2.0 for compatibility with Xamarin.Forms, ...

### Version 2.1.1.0 - 21/02/2025
* ObservableObject
* new implementation of BaseViewModel
  *  add implementation of Singleton
  *  add commands

```csharp
public class yourViewModel : BaseViewModel<yourViewModel>
{
   public ICommand SimpleCommand { get; } 

   public yourViewModel()
   {
      SimpleCommand = new RelayCommand(ExecuteSimpleCommand, CanExecuteSimpleCommand);
   }

   public string Hello()
   {
      return "Hello World!";
   }

   public string Toto { get => _toto; set => SetField(ref _toto, value); }
   string _toto = "toto";


   private void ExecuteSimpleCommand(object parameter)
   {
      // Your command execution logic here
      Console.WriteLine("SimpleCommand executed with parameter: " + parameter);
   }

   private bool CanExecuteSimpleCommand(object parameter)
   {
      // Your logic to determine if the command can execute
      return true; // or some condition
   }
}


public class yourClass
{
   public void yourCode()
   {
      yourViewModel.Current.Hello();

      yourViewModel.Current.Toto = "titi";
   }
}
```

### Version 2.0.0.8 - 29/10/2020
 * Add: AuditTrail.WithStack() & AuditTrail.FromHere()


### Version 1.1.11 - 05/2020
 * Add: NameValue_DateTime


### Version 1.1.10 - 09/2019
 * Add: DB_Attributes.TableNameAttribute
 * Add: EnumerableExtensions


### Version 1.1.9 - 08/2019
 * NameValue: override string ToString()
 * Open source ...
 * Code review ...
 * Add some unit tests ...
   

### Version 1.1.6 - 07/2019  
 * Comming out ...
