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
		echo "hi monish";
	}
}

view:

---------------home.php----------------


<?php $hi ?>
<?php $hi ?>


output:

