# SettingsActivity

## Ejemplo en el que se utiliza una Actividad para mostrar los ajustes.

Enlaces relacionados:

[https://developer.android.com/training/data-storage/shared-preferences](https://developer.android.com/training/data-storage/shared-preferences)

[https://developer.android.com/guide/topics/ui/settings](https://developer.android.com/guide/topics/ui/settings)

En el manifiesto de declara el padre de la SettingsActivity:

> &lt;activity android:name=".AjustesActivity"  
    android:label="@string/title_activity_ajustes"  
    **android:parentActivityName=".MainActivity"**/&gt;

En la actividad de ajustes se obtiene la barra de actividad y se activa la vuelta a la actividad padre:

> @Override  
protected void onCreate(Bundle savedInstanceState) {  
 ...  
 ActionBar actionBar = getSupportActionBar();  
 if (actionBar != null) {  
  actionBar.setDisplayHomeAsUpEnabled(true);  
 }  
}
