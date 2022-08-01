# laravel9_change_date_format
## 1. Laravel 9 Change Date Format with Model
```Dockerfile
<?php
namespace App\Http\Controllers;
  
use Illuminate\Http\Request;
use App\Models\User;
  
class DemoController extends Controller
{
    /**
     * Write code on Method
     *
     * @return response()
     */
    public function index()
    {
        $user = User::first();
        $newDate = $user->created_at->format('d-m-Y');
        
        dd($newDate);
    }
}
```
- Output: 11-02-2022
## 2. Laravel 9 Change Date Format Y-m-d H:i:s to d-m-Y
```Dockerfile
<?php
  
namespace App\Http\Controllers;
   
use Illuminate\Http\Request;
use Carbon\Carbon;
  
class DemoController extends Controller
{
    /**
     * Write code on Method
     *
     * @return response()
     */
    public function index()
    {
        $date = date('Y-m-d H:i:s');
        $newDate = Carbon::createFromFormat('Y-m-d H:i:s', $date)
                                    ->format('m/d/Y');
        dd($newDate);
    }
}
```
- Output: 02/17/2022
## 3. Laravel 9 Change Date Format Y-m-d to m/d/Y
```Dockerfile
<?php
  
namespace App\Http\Controllers;
  
use Illuminate\Http\Request;
use Carbon\Carbon;
   
class DemoController extends Controller
{
    /**
     * Write code on Method
     *
     * @return response()
     */
    public function index()
    {
        $date = "2022-02-22";
        $newDate = Carbon::createFromFormat('Y-m-d', $date)
                                ->format('m/d/Y');
  
        dd($newDate);
    }
}
```
- Output: 02/22/2022
## 4. Laravel 9 Change Date Format m/d/Y to Y-m-d
```Dockerfile
<?php
  
namespace App\Http\Controllers;
  
use Illuminate\Http\Request;
use Carbon\Carbon;
 
class DemoController extends Controller
{
    /**
     * Write code on Method
     *
     * @return response()
     */
    public function index()
    {
        $date = "02/22/2022";
        $newDate = Carbon::createFromFormat('m/d/Y', $date)
                            ->format('Y-m-d');
  
        dd($newDate);
    }
}
```
- Output: 2022-02-22
## 5.  Laravel 9 Change Date Format Y-m-d to d/m/Y
```Dockerfile
<?php
  
namespace App\Http\Controllers;
  
use Illuminate\Http\Request;
use Carbon\Carbon;
  
class DemoController extends Controller
{
    /**
     * Write code on Method
     *
     * @return response()
     */
    public function index()
    {
        $date = "2022-02-22";
        $newDate = Carbon::createFromFormat('Y-m-d', $date)
                             ->format('d/m/Y');
  
        dd($newDate);
    }
}
```
- Output: 22/02/2022
