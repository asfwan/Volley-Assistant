# Volley-Assistant
An extension to the famous Android Volley

How to use?

GET method:

```java
  Map<String,String> params = new HashMap<String, String>();
  params.put(KEY_USERNAME,username);
  params.put(KEY_PASSWORD,password);
  params.put(KEY_EMAIL, email);

  VolleyAssistant.init(this).Get("http://example.com/endpoint", params, new Response.Listener() {
      @Override
      public void onResponse(Object response) {
              Toast.makeText(MainActivity.this,response.toString(), Toast.LENGTH_LONG).show();
          }
      }, new Response.ErrorListener() {
      @Override
      public void onErrorResponse(VolleyError error) {
              Toast.makeText(MainActivity.this,error.toString(),Toast.LENGTH_LONG).show();
          }
      });
```

POST method:
```java
  Map<String,String> params = new HashMap<String, String>();
  params.put(KEY_USERNAME,username);
  params.put(KEY_PASSWORD,password);
  params.put(KEY_EMAIL, email);

  VolleyAssistant.init(this).Post("http://example.com/endpoint", params, new Response.Listener() {
      @Override
      public void onResponse(Object response) {
              Toast.makeText(MainActivity.this,response.toString(), Toast.LENGTH_LONG).show();
          }
      }, new Response.ErrorListener() {
      @Override
      public void onErrorResponse(VolleyError error) {
              Toast.makeText(MainActivity.this,error.toString(),Toast.LENGTH_LONG).show();
          }
      });
```
