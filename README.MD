<h1>ID GENERATOR USER GUIDE</h1>

<h2>License Agreement</h2>
<h4>The BSD 3-Clause License</h4>

<blockquote>

 
    <p>Copyright &copy; 2016, MITOS<br>
     All rights reserved.</p>

    <p>Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:</p>

    <p>1. Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.</p>
    <p>2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.</p>
    <p>3. Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.</p>

    <p>THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.</p>
  </div>
</blockquote>

<h2>Change Log</h2>


<h2>Welcome to IdGenerator</h2>
<blockquote>

 
    <p>IdGenerator is an Library generator for CodeIgniter  - a toolkit - for people who build web sites using PHP. Its goal is to enable you to develop projects much faster than you could if you were writing code from scratch, by providing a rich set of libraries for commonly needed tasks, as well as a simple interface and logical structure to access these libraries. IdGenerator lets you creatively focus on your project by minimizing the amount of code needed for a given task.</p>

</blockquote>

<h2>Why IdGenerator ? </h2>
<p>IdGenerator it is a totally different idea and... more simple idea! With few simple PHP lines of code you can have all the functionality that you need to create your CRUD. So this means you <b>don't</b> have to copy the same Javascripts,CSS, views,models,vaildation rules,html code, grid, upload functionality ... e.t.c . again and again. To create again a CRUD for a different table you will just need simple PHP lines of code. </p><br>
<p>The good part is that you don't even have to change the CSS to make it more user friendly. IdGenerator is ready for the production mode with all the required security and views.</p><br>
<p><b>IdGenerator is an automatic CRUD generator</b> and it can cover almost all your needs for a CRUD system (simple or complex one) as it has many features and still keep going.</p><br>
<p>Some of the main features of IdGenerator  are:</p>
<ul class="with-arrows">
	<li>Datagrid listing with paging, sorting, searching by field and search for all with ajax (flexigrid theme) or instant javascript scripting (datatables theme)</li>
	<li>Automatic creation of inputs by field type. Till now the field types that auto-generate different inputs are: integer, string, text, date, datetime, set, enum, true_false(0 or 1), hidden, password and readonly</li>
	<li>Database relation 1-1 , 1-n and n-n , automatically with just one line of code</li>
	<li>Changing themes easlily, so far there are two themes , datatables and flexigrid</li>
	<li>Validation form with client side validation and server side validation</li>
	<li>Flexibility to choose columns and fields that you want to add to your table</li>
	<li>Unset operation like unset add, edit or delete</li>
	<li>Changing the auto generate field type, for example a text field can transform easily to date field</li>
	
</li>
</ul>

<h2>Server Requirements</h2>
<p><a class="reference external" href="http://php.net/">PHP</a> version 5.4 or newer is recommended.</p>
<p>It should work on 5.2.4 as well, but we strongly advise you NOT to run
such old versions of PHP, because of potential security and performance
issues, as well as missing features.</p>
<p>A database is required for most web application programming.
Currently supported databases are:</p>
<blockquote>
<div><ul class="simple">
<li>MySQL (5.1+) via the <em>mysql</em> (deprecated), <em>mysqli</em> and <em>pdo</em> drivers</li>
<li>Oracle via the <em>oci8</em> and <em>pdo</em> drivers</li>
<li>PostgreSQL via the <em>postgre</em> and <em>pdo</em> drivers</li>
<li>SQLite via the <em>sqlite</em> (version 2), <em>sqlite3</em> (version 3) and <em>pdo</em> drivers</li>
<li>CUBRID via the <em>cubrid</em> and <em>pdo</em> drivers</li>
<li>Interbase/Firebird via the <em>ibase</em> and <em>pdo</em> drivers</li>
<li>ODBC via the <em>odbc</em> and <em>pdo</em> drivers (you should know that ODBC is actually an abstraction layer)</li>
</ul>
</div></blockquote>


<h2>Installation for Codeigniter </h2>

<p>
    The installation is really easy. You just copy <b>all the files</b> to your project and you are ready to use IdGenerator.
</p>
<p>
    By the end of the installation, your file structure should look similar to this (the below structure is the default unchanged folders/files of codeigniter.
</p><div class="code">
    website_folder/
    <br>–––– application/
    <br>–––––––– config/
    <br>–––––––––––– i_generator.php
    <br>–––––––––––– ...
    <br>–––––––– controllers/
    <br>–––––––––––– ...
    <br>–––––––– libraries/
    <br>–––––––––––– igenerator/
    <br>––––––––––––---- I_Form.php
    <br>––––––––––––---- I_Generator.php
    <br>––––––––––––---- I_GeneratorBridge.php
    <br>––––––––––––---- I_Grid.php
    <br>––––––––––––---- I_Pagination.php
    <br>––––––––––––---- I_Table.php
    <br>––––––––––––---- I_Template.php
    <br>––––––––––––---- I_Upload.php
    <br>–––––––––––– ...
    <br>–––––––– models/
    <br>–––––––––––– ...
    <br>–––––––– views/
    <br>–––––––––––– template/
    <br>––––––––––––---- tpl_default.php
    <br>––––––––––––---- tpl_scripts.php
    <br>–––– common/
    <br>–––––––– bootstrap/
    <br>–––––––– fonts/
    <br>–––––––– jquery/
    <br>–––––––– plugins/
    <br>–––––––– theme/
    <br>–––––––– uploads/
    <br>–––– system/
</div>
<p></p>
<h4>application/config/autoload.php</h4>
<figure class="highlight"><pre><code class="php">
<span>$autoload['libraries'] = array('database','session','igenerator/I_Generator');</span>
</code></pre></figure>  
<h4>application/views/template/tpl_default.php (Default Template)</h4>
<figure class="highlight"><pre><code class="html">
<figure class="highlight"><pre><code class="html">
&lt;!DOCTYPE html&gt;
&lt;html lang="id"&gt;
    &lt;head&gt;
        &lt;meta charset="utf-8"/&gt;
        &lt;meta http-equiv="X-UA-Compatible" content="IE=edge"&gt;
        &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"/&gt;
        &lt;title&gt;ID GENERATOR&lt;/title&gt;
        
        &lt;!-- START REQUIRED --&gt;
        &lt;link rel="stylesheet" href="&lt;?php echo base_url(common/bootstrap/css/bootstrap.css); ?&gt;"/&gt;
        &lt;link rel="stylesheet" href="&lt;?php echo base_url(common/theme/css/i_generator.css); ?&gt;"/&gt;
        &lt;link rel="stylesheet" href="&lt;?php echo base_url(common/plugins/validator/css/bootstrapValidator.min.css); ?&gt;"/&gt;
        &lt;link rel="stylesheet" href="&lt;?php echo base_url(common/fonts/font-awesome/css/font-awesome.min.css); ?&gt;"/&gt;
        &lt;link rel="stylesheet" href="&lt;?php echo base_url(common/plugins/fileinput/css/fileinput.css); ?&gt;"/&gt;
        &lt;link rel="stylesheet" href="&lt;?php echo base_url(common/theme/css/animate.css); ?&gt;"/&gt;
        &lt;!-- HTML5 shim and Respond.js for IE8 support of HTML5 elements and media queries --&gt;
        &lt;!-- WARNING: Respond.js doesnt work if you view the page via file:// --&gt;
        &lt;!--[if lt IE 9]&gt;
        &lt;script src="https://oss.maxcdn.com/html5shiv/3.7.2/html5shiv.min.js"&gt;&lt;/script&gt;
        &lt;script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"&gt;&lt;/script&gt;
        &lt;![endif]--&gt;
        &lt;script src="&lt;?php echo base_url(common/jquery/jquery-2.2.0.min.js); ?&gt;"&gt;&lt;/script&gt;
        &lt;script src="&lt;?php echo base_url(common/plugins/fileinput/js/fileinput.js); ?&gt;"&gt;&lt;/script&gt;
        &lt;!-- END REQUIRED --&gt;
    &lt;/head&gt;

    &lt;body&gt;
        
        &lt;!-- START REQUIRED --&gt;
        &lt;div class="notifications top-right"&gt;&lt;/div&gt;
        &lt;div class="i_progress"&gt;
            &lt;div class="progress progress-striped active"&gt;&lt;div class="progress-bar progress-bar-primary" role="progressbar" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100" style="width: 0%;"&gt;&lt;/div&gt;&lt;/div&gt;
        &lt;/div&gt;
        &lt;div class="modal fade" id="modal"&gt;
            &lt;div class="modal-dialog"&gt;
                &lt;div class="modal-content"&gt;
                    &lt;div class="modal-header"&gt;
                        &lt;button type="button" class="close" data-dismiss="modal" aria-label="Close"&gt;&lt;span aria-hidden="true"&gt;&amp;times;&lt;/span&gt;&lt;/button&gt;
                        &lt;h4 class="modal-title"&gt;&lt;/h4&gt;
                    &lt;/div&gt;
                    &lt;div class="modal-body"&gt;
                        &lt;p&gt;&lt;/p&gt;
                    &lt;/div&gt;
                    &lt;div class="modal-footer"&gt;
                    &lt;/div&gt;
                &lt;/div&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        &lt;!-- END REQUIRED --&gt;
        
        
        &lt;div class="container"&gt;
            &lt;!-- START REQUIRED --&gt;
            &lt;?php if ($this-&gt;session-&gt;flashdata("status")): ?&gt;
                &lt;div class="alert alert-&lt;?php echo $this-&gt;session-&gt;flashdata("status"); ?&gt; alert-dismissible" role="alert"&gt;
                    &lt;button type="button" class="close" data-dismiss="alert" aria-label="Close"&gt;&lt;span aria-hidden="true"&gt;&amp;times;&lt;/span&gt;&lt;/button&gt;
                    &lt;strong&gt;&lt;?php echo ucfirst($this-&gt;session-&gt;flashdata("title")); ?&gt;&lt;/strong&gt; &lt;?php echo ucfirst($this-&gt;session-&gt;flashdata(message)); ?&gt;
                &lt;/div&gt;
            &lt;?php endif; ?&gt;
            &lt;!-- END REQUIRED --&gt;
            &lt;!-- START REQUIRED //DO NOT RENAME ATTRIBUTE CLASS! --&gt;
            &lt;div class=contents&gt;
                &lt;?php echo isset($contents) ? $contents : ""; ?&gt;
            &lt;/div&gt;
            &lt;!-- END REQUIRED --&gt;

        &lt;/div&gt;
        
        
        &lt;!-- START REQUIRED --&gt;
        &lt;script src="&lt;?php echo base_url(common/bootstrap/js/bootstrap.min.js); ?&gt;"&gt;&lt;/script&gt;
        &lt;script src="&lt;?php echo base_url(common/plugins/validator/js/bootstrapValidator.min.js); ?&gt;"&gt;&lt;/script&gt;
        &lt;script src="&lt;?php echo base_url(common/plugins/bootbox/js/bootbox.min.js); ?&gt;"&gt;&lt;/script&gt;
        &lt;?php $this-&gt;load-&gt;view(template/tpl_scripts); ?&gt;
        &lt;!-- END REQUIRED --&gt;
    &lt;/body&gt;
&lt;/html&gt;</code></pre></figure>
</code></pre></figure>  

For more example see our <a href="http://idgenerator.mitos.or.id" target="_blank">Example Page</a>
