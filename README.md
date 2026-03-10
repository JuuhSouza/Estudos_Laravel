## Aprendendo Rotas e Controllers no Laravel

Nesta etapa do projeto, configurei uma rota personalizada que chama um método dentro de um Controller para listar séries.

### 1. Configurando a Rota
No arquivo `routes/web.php`, adicionei a rota que aponta para o método `listarSeries`:

```php
use Illuminate\Support\Facades\Route;
use App\Http\Controllers\SeriesController;

Route::get('/', function () {
    return view('welcome');
});

/* Aprendendo rotas */
Route::get('/series', [SeriesController::class, 'listarSeries']);
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

<?php
