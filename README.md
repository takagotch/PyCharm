### pycharm
---
https://github.com/JetBrains/intellij-community/tree/master/python

https://www.jetbrains.com/pycharm/

```py
// python/pluginCore/com/jetbrains/python/packaging/PyManagePackagesAction.java

public class PyManagePackagesAction extends AnAction {
  @Override
  public void actionPerformed(@NotNull AnActionEvent e) {
    Module module = e.getData(LangDataKeys.MODULE);
    final Sdk sdk = PythonSdkType.findPythonSdk(module);
    if (module != null && sdk != null) {
      new PyManagePackagesDialog(module.getProject(), sdk).show();
    }
  }
  
  @Override
  public void update(@NotNull AnActionEvent e) {
    Module module = e.getData(LangDataKeys.MODULE);
    e.getPresentation().setEnabled(module != null && PythonSdkType.findPythonSdk(module) != null);
  }
}
```

```
```

```
```

