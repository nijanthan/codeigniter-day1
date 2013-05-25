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







how to delete index option

  -------routine.php-----
$route['default_controller'] = "nijan";
---------config.php--------

$config['base_url']	= 'http://localhost/day/codeday1/index.php';



