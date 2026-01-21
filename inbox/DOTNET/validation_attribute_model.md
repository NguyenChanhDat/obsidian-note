---
topic: 
date: "2026-01-21"
course: 
tags:
  - studies
---

# validation_attribute_model

## Key Concepts

Validation attributes let you specify validation rules for model properties. The following example from the [sample app](https://github.com/dotnet/AspNetCore.Docs/tree/main/aspnetcore/mvc/models/validation/samples) shows a model class that is annotated with validation attributes. The `[ClassicMovie]` attribute is a custom validation attribute and the others are built in. Not shown is `[ClassicMovieWithClientValidator]`, which shows an alternative way to implement a custom attribute.

C#

```C#
public class Movie
{
    public int Id { get; set; }

    [Required]
    [StringLength(100)]
    public string Title { get; set; } = null!;

    [ClassicMovie(1960)]
    [DataType(DataType.Date)]
    [Display(Name = "Release Date")]
    public DateTime ReleaseDate { get; set; }

    [Required]
    [StringLength(1000)]
    public string Description { get; set; } = null!;

    [Range(0, 999.99)]
    public decimal Price { get; set; }

    public Genre Genre { get; set; }

    public bool Preorder { get; set; }
}
```
## Important Details


## Examples


## References

https://learn.microsoft.com/en-us/aspnet/core/mvc/models/validation?view=aspnetcore-10.0

## Related Topics
- [[DOTNET]]