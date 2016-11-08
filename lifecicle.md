#Life cycle de Activity Android


###Criando uma nova Instância
```
@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);


        Log.d("meuLog","Evento Abriu Cena!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!");
    }
``` 

***

###Saindo do APP minimizando etc
```
  @Override
    protected void onStop() {
        super.onStop();
        Log.d("meuLog", "Evento Saindo do App!!!!!!!!!!!!!!!!!!!!!!!!");
    }

```
***

###Tocando na activity
```
 @Override
    public boolean onTouchEvent(MotionEvent event) {
        Log.d("meuLog","Evento Tocou na Cena!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!");
        return super.onTouchEvent(event);
    }
```
***

###Executada após o onCreate() ou onRestart() 
``` 
 @Override
    protected void onStart() {
        super.onStart();
        Log.d("meuLog", "Evento Abriu App!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!");
    }

```
***

###Quanto o sistema está prestes a começar a retomar outra atividade
``` 
   @Override
    protected void onPause() {
        super.onPause();Log.d("meuLog", "Evento PAUSOU O APP!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!");
    }
```
***

```
### Quando a Activity começa a interagir com o usuário
 @Override
    protected void onResume() {
        super.onResume(); Log.d("meuLog", "Evento VOLTOU PARA O APP!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!");
    }
```
***


### Quando a activity parou por algum motivo e foi resetada
```
   @Override
    protected void onRestart() {
        super.onRestart();
    }
```
***

###  Metodo responsavel por liberar a activity da memória
```
     @Override
    protected void onDestroy() {
        super.onDestroy();
    }
```
***