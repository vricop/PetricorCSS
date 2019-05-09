## Todo

 - [ ] Configure class names for your breakpoints prefixes. You can use any valid
       css you want. Then you set your breakpoint ???
 - [ ] Add `group-hover` prefix for variants eg:

   ```css
     *:hover .group-hover\:{$variang}:hover { … }
   ```

   ```html
     <div>
       <a class="group-hover:{$variant}:hover" href="#">Link</a>
     </div>
   ```
 - [ ] Rename '$modules' config for '$variants'.
 - [ ] Improve config file