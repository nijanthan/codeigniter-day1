codeigniter-day1
================

codeigniter day 1


controller:

----------------nian.php--------------

<?php 


class nijan extends CI_Controller
{
  function index()
	{
		$data['hi']="hi da nijssssan";
                $data['ji']="hi da nijssssan";
		
		echo "hello world";
		
		
		
		$this->load->view('home',$data);
		}
	function monish()
	{
	
	      $nijan['nijan']="hi da nijan";
	      
	      
	
		echo "hi monish";
	}
}

view:

---------------home.php----------------


<?php $hi ?>
<?php $hi ?>
---------------about.php--------------


<?php $nijan ?>

output:
hi da nijssssan







how to delete index.php option --config file

  -------routine.php-----
$route['default_controller'] = "nijan";
---------config.php--------

$config['base_url']	= 'http://localhost/day/codeday1/index.php';







how to get data from data base:



------------------controller-------------------
nijan.php


<?php 


class Nijan extends CI_Controller
{
	function index()
	{

		$this->load->model('site_model');
		
		$data['nijan12']=$this->site_model->getAll();
		$this->load->view('home',$data);
		
	}
}


-------------------------model------------------------------

model.php


<?php


class Site_model extends  CI_Model
{
	function getAll(){
	
	
		
		$q = $this->db->get('nijan');
		
	
		foreach ($q->result() as $row)
		{
		$data[]=$row;
		}
		return $data;
		}
	
	
-------------------------view-------------------
<?php ?>
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
<title>Insert title here</title>
</head>
<body>
 
</br>
<h1>nijan hi da</h1> 
<pre>

<?php  print_r($nijan12)?>


or

<div><?php foreach ($nijan12 as $row):?>
<h1><?php echo $row->title; ?> </h1>
<?php endforeach;?>
</pre>
</body>
</html>

------------------------autoload add('database')--------------------

 
 2.
 
database -->ci_series -->data--> id ,author,title
database -->ci_series -->test -->id ,title

------------------------------controller----------------------
nijan.php
<?php
class nijan1 extends CI_Controller{
	
	function index(){
	
	$this->load->model('Data_model');
   $data['rows']=$this->Data_model->getAll();	
	$this->load->view('home', $data);
	}

}

------------------------------model-----------------------
Data_model.php

<?php
class Data_model extends CI_Model
{
	
	function getAll() {
 $q=$this->db->query("SELECT * FROM data");
		
if($q->num_rows()>0){ 
	foreach($q->result() as $row)
	
	$data[]=$row;
	}
	
	return $data;
	
	}	
	
}

---------------------------view------------------------------
home.php


<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
<title>Insert title here</title>
</head>
<body>
<div><?php foreach ($rows as $r){
	echo $r->author;
	echo '<h1>'. $r->title. '</h1>'.'</br>';

echo $r->id;


}
?>

</div>
</body>
</html>







