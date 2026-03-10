# 🎬 Projeto Estudos Laravel

Documentação do aprendizado sobre Rotas e Controllers.

## 📍 1. Configurando as Rotas
As rotas são responsáveis por receber a requisição do navegador. O arquivo editado foi o `routes/web.php`.

```php
use Illuminate\Support\Facades\Route;
use App\Http\Controllers\SeriesController;

Route::get('/', function () {
    return view('welcome');
});

/* Rota que chama o Controller de Séries */
Route::get('/series', [SeriesController::class, 'listarSeries']);

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
