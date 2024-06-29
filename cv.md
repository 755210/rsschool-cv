![logo](logo.png)
# Andrey Shcherbakov
* __Email__ 755210@gmail.com
* __Discord__ Andrey (@755210)
## Brief Self-Introduction
My goals - professional development
## Skils
Tehnological platform 1C: Enterprise
## Work Experience
Development according to customer requirements
## Code Examples
``` 1C: Enterprise
// Prosedure - Compare
// For files listed in tables, opens the WinMerge application
&AtClient
Prosedure Compare()	
	i =0;	
	While True Do		
		Strings1 = VT_Old.SearchStrings(New Structure("Number",i));
		Strings2 = VT_New.SearchStrings(New Structure("Number",i)); 		
		If Strings1.Quantity() > 0 OR Strings2.Quantity() > 0  Then			
			For = ?(Strings1.Quantity() > Strings2.Quantity(), Strings1.Quantity(), Strings2.Quantity());			
			For y = 0 To For-1 Do				
				If Strings1.Quantity() > 0 AND Strings1.Quantity() > y Then				
					Str1 = Strings1[y].Path;	
				Else
					Str1 = "";
				EndIf;				
				If Strings2.Quantity() > 0 AND Strings2.Quantity() > y Then				
					Str2 = Strings2[y].Path;	
				Else
					Str2 = "";
				EndIf;                				
				If Str1 = "" AND Str2 = "" OR NOT (Strings1[y].ThereIsADifference AND Strings2[y].ThereIsADifference) Then
					Continue;			
				EndIf;		
					CommandString = PathWinMerge + " " + Str1 + " " + Str2; 
					LaunchTheApplication(CommandString);						
			EndDo;			
		Else
			Breack;
		EndIf;		
	    i = i + 1;		
	EndDo;				
EndProcedure
```
## Education
Novosibirsk State Technical University - (Computer Sience) Software Engineering
## English Language 
Elementary