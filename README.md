<?php
  require('db.php');
  $query="Select * from location";
  $result=mysqli_query($con,$query);
  while($row = mysqli_fetch_array($result)) 
  {        
  echo "<option value='".$row['location']. "'>" . $row['location'] . "</option>"; 
  }
  echo "</select> <p>Select a product:</p>";

  $query2="Select * from product";
  $result2=mysqli_query($con,$query2);
  while($row2= mysqli_fetch_array($result2)) 
  {        
  echo "<input type='checkbox' id='product' name='product[]' value='".$row2['product']. "'>" .$row2['product']."<br>"; 

  }
?>
<?php
require('db.php');
$query="Select * from hotel";
$result=mysqli_query($con,$query);
while($row = mysqli_fetch_array($result))
{
echo "<option value='" .$row['room_type']. '- Â£'. $row['price']."'>" . $row['room_type']. "- Â£" . $row['price'] ."</option>";
}
