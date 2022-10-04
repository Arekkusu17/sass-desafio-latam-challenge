# Challenge Sass - Desafio Latam

The meaning of this challenge is to validate Sass knowledge applying styles to improve and make faster the design of a web.

Site of deploy: https://arekkusu17.github.io/sass-desafio-latam-challenge/
## Work Done
- Write the html structure and use the card class from bootstrap.
All the Sass and Bootstrap changes are in the custom.scss file.    
- Change the base font to 'Dancing Script', cursive. (line 2)
    ~~~
    $font-family-base: 'Dancing Script', cursive;
    ~~~
- Create new variables for custom colors and add them to the `$theme-colors`, (line 16-17-32-33)  
    ~~~
    $purple: #cf649a;
    $pastel-pink: #ebc3ec;

    $theme-colors: (
        ...
        "purple":     $purple,
        "pastel":     $pastel-pink
    );
    ~~~
- Create some classes using @extend propertie to reuse some classes (line 52-60)
    ~~~
    .card-black {
        @extend .card;   
        background: rgb(31, 31, 31);
        color: white;
    }
    ~~~
- use @mixin to create new btn styles where you write the text-color and background-color (line 69)
    ~~~
    @mixin btn($bg-color,$color){
        background-color: $bg-color;
        color: $color; 
        @extend .p-2;
        border: none;
        border-radius: 5px;
        &:hover {
        opacity: 0.8;
        } 
    }

    .btn-purple{
        @include btn($purple,$white)
    }
    ~~~
- Fix some typos and add README.md
