## Adicionando listas no Controller

Nesta etapa, criei um método no `SeriesController` para listar nomes de séries e retornar o HTML diretamente para a rota.

```php
<?php  

namespace App\Http\Controllers;

class SeriesController
{
    public function listarSeries()
    {
        $series = [
            'Lost',
            'Game of Thrones',
            'See'
        ];

        $html = '<ul>';

        foreach ($series as $serie) {
            $html .= "<li>$serie</li>";
        }

        $html .= '</ul>';

        return $html;
    }
}
