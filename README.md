# Persistent Helper
Easy way to persist any objects when Android screen rotation

![Logo](https://www.google.ro/url?sa=i&rct=j&q=&esrc=s&source=images&cd=&cad=rja&uact=8&ved=&url=https%3A%2F%2Fplus.google.com%2F106756573004662205914&bvm=bv.118443451,d.bGQ&psig=AFQjCNExrVmR4kajD0MKfyzo6ErqxiL_VQ&ust=1459597010446781)

By using this app you eliminate lot of code that is used for saving data when screen orientation changes

Use the following code to save and restore data:

```java
public class ExampleFragment extends Fragment {
    @Persistent
    private Object javaObject;
    @Persistent
    private int currentPosition;

    @Override
    public void onSaveInstanceState(Bundle outState) {
        super.onSaveInstanceState(outState);
        PersistentHelper.saveState(this, outState, Fragment.class);
        //javaObject and currentPosition saved
    }

    @Override
    public void onViewCreated(View view, Bundle savedInstanceState) {
        super.onViewCreated(view, savedInstanceState);
        PersistentHelper.restoreState(this, savedInstanceState, Fragment.class);
        //javaObject and currentPosition restored
    }
    ```
    
    For additional information mailto: dunatv@gmail.com
