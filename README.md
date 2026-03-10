###Adicionado listas no controller

namespace App\Http\Controllers;

class SeriesController{
    public function listarSeries(){
        $series = [
         'Lost',
         'Game of thrones',
         'See'
        ];

        $html = '<ul>';

        foreach($series as $series){
            $html .="<li>$series</li>";
        }

        echo $html;
    }
}
