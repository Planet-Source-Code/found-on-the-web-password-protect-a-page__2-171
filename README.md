<div align="center">

## Password protect a page


</div>

### Description

How can I password protect a page? The simplist and most effective password protection using just clientside JavaScripting, relies on the user not knowing the target filename.

Found on the web at:http://www.irt.org
 
### More Info
 
Where frameName1 and frameName2 are the names of the two frames that you want to change.



Note, the user can find the directory location, by examining the source, therefore you must protect your directory by placing a default file inside it, which your server will always send when the directory is requested, e.g. index.html, otherwise a directory listing will be sent.

It is also possible on Unix systems, to just set the parent (or all) directory's permissions to rwx--x--x and all other files to rwxr--r--. The user cannot get directory listings, but can still access any files there. (Thanks to Mike Crawford for this last tip.)


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Found on the Web](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/found-on-the-web.md)
**Level**          |Unknown
**User Rating**    |6.0 (601 globes from 101 users)
**Compatibility**  |
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__2-57.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/found-on-the-web-password-protect-a-page__2-171/archive/master.zip)





### Source Code

```
<SCRIPT LANGUAGE="JavaScript"><!--
function go() {
  window.location.href = "http://www.somewhere.com/" +
    document.formName.passwordName.value + '.html';
  return false;
}
//--></SCRIPT>
<FORM NAME="formName" onSubmit="return go()">
Enter Password: <INPUT TYPE="password" NAME="passwordName" VALUE="" SIZE=8>
</FORM>
```

