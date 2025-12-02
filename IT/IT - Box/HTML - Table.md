```html
<table border="1"> <!--Table-->
	<caption>People</caption> <!--Caption-->
	<colgroup>
		<col span="1"> <!--Colgroup-->
		<col span="1" style="background-color: blue">
		<col span="1" style="visibility: collapse"> <!--Hide Row-->
	</colgroup>
	<tr> <!--Row-->   
		<th colspan="2">Name</th>  
		<th>Age</th> <!--Header--> 
	</tr>  
	
	<tr>  
		<td>Jill</td> <!--Cell--> 
		<td>Smith</td>  
		<td rowspan="2">50</td>  
	</tr> 
	 
	<tr>  
		<td>Eve</td>  
		<td>Jackson</td>  
	</tr>
	<tr>  
		<td>Cal</td> 
		<td>Newport</td>
		<td>60</td>  
	</tr>
</table>
```