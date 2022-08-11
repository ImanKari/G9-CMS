<a href="https://www.nuget.org/profiles/ImanKari"><img src="https://github.com/ImanKari/G9JSONHandler/blob/main/G9JSONHandler/G9JSONHandler/G9-Icon.png?raw=true" width="50"/> <label style="position: relative; top: -6.9px;font-size: 39.9px">G9JSONHandler</label></a>

[![NuGet version (G9JSONHandler)](https://img.shields.io/nuget/v/G9JSONHandler.svg?style=flat-square)](https://www.nuget.org/packages/G9JSONHandler/)
[![Build Status](https://g9tm.visualstudio.com/G9JSONHandler/_apis/build/status/G9JSONHandler?branchName=main)](https://g9tm.visualstudio.com/G9JSONHandler/_build/latest?definitionId=14&branchName=main)

# G9JSONHandler is a pretty small library for JSON.

## Object To JSON

```csharp
Product product = new Product();
product.Name = "Apple";
product.Expiry = new DateTime(2008, 12, 28);
product.Sizes = new string[] { "Small" };

string json = JsonConvert.SerializeObject(product);
// {
//   "Name": "Apple",
//   "Expiry": "2008-12-28T00:00:00",
//   "Sizes": [
//     "Small"
//   ]
// }
```

## JSON To Object

```csharp
string json = @"{
  'Name': 'Bad Boys',
  'ReleaseDate': '1995-4-7T00:00:00',
  'Genres': [
    'Action',
    'Comedy'
  ]
}";

Movie m = JsonConvert.DeserializeObject<Movie>(json);

string name = m.Name;
// Bad Boys
```
