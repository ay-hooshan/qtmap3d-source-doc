
# Functions

## main.cpp - Complete

---
#### int main(int argc, char *argv[]);

**parameters**
:
  - **argc**: arguments count
  - **argv**: arguments values

**description**
: CPP program starter

## application.cpp

### Application

- singleton class!
- base code for final program

---
#### explicit Application();

**parameters**
:

**description**
: **private** class constructor that initial just new for mPluginManager

---
#### static Application *instance();

**parameters**
:

**description**
: create a static instance from class and returns its address

---
#### static void performStartupConfiguration();

**parameters**
:

**description**
: do some important configurations: set platform theme for ui, initialSurfaceFormat()

---
#### void initialize();

**parameters**
:

**description**
: prepare MainWindow and ListWindow, initializeQmlEngine(), initializeDefenseDataManager(), prepare mQmlEngine for program

---
#### void show();

**parameters**
:

**description**
: show mMainWindow

---
#### inline MainWindow *mainWindow() const;

**parameters**
:

**description**
: getter for mMainWindow

---
#### inline QQmlApplicationEngine *qmlEngine() const;

**parameters**
:

**description**
: getter for mQmlEngine

---
#### inline DefenseDataManager *defenseDataManager() const;

**parameters**
:

**description**
: getter for mDefenseDataManager

---
#### ServiceManager *serviceManager() const;

**parameters**
:

**description**
: getter for mServiceManager

---
#### static void initialSurfaceFormat();

**parameters**
:

**description**
: creating and setting as default a surface format for QSurfaceFormat class.

---
#### void initializeQmlEngine();

**parameters**
:

**description**
: initializing mQmlEngine

---
#### void initializeDefenseDataManager();

**parameters**
:

**description**
: initialize mDefenseDataManager

---
#### void onQmlObjectCreated(QObject *obj, const QUrl &objUrl);

**parameters**
:
  - **obj**: created object pointer
  - **objectUrl**: object url reference

**description**
: set mMainWindow and mListWindow when created (?)

---
#### void onUICreated();

**parameters**
:

**description**
: preparing map item as a service (?)

## mainwindow.cpp

### MainWindow

---
#### MainWindow(QWindow *parent = nullptr);

**parameters**
:
  - **parent**: parent pointer

**description**
: class constructor, initializing mToolbox, registering
MapControllerItem, SmallMap for qml

---
#### void initComponent();

**parameters**
:

**description**
: initializing mMapItem, mLayersModel, mLocationManagerProxyModel

---
#### QQmlEngine *getQmlEngine();

**parameters**
:

**description**
: getter for qml engine

---
#### LayersModel *layersModel() const;

**parameters**
:

**description**
: getter for mLayersModel

---
#### ToolboxProxyModel *toolbox() const;

**parameters**
:

**description**
: getter for mToolbox

---
#### LocationManagerProxyModel *locationManagerProxyModel() const;

**parameters**
:

**description**
: getter for mLocationManagerProxyModel

---
#### MapItem* getMapItem();

**parameters**
:

**description**
: getter for mMapItem

---
#### void addToLeftContainer(QQuickItem *item, QString title);

**parameters**
:
  - **item**: qml item pointer to add in sidebar
  - **title**: title that is shown in top tab

**description**
: call a qml function that add item to left sidebar

---
#### void addToRightContainer(QQuickItem *item, QString title);

**parameters**
:
  - **item**: qml item pointer to add in sidebar
  - **title**: title that is shown in top tab

**description**
: call a qml function that add item to right sidebar

---
#### void addToCenterCenterContainer(QQuickItem *item);

**parameters**
:
  - **item**: qml item pointer to add to main window

**description**
: call a qml function that add item to main window

---
#### void removeFromLeftContainer(QQuickItem *item);

**parameters**
:
  - **item**: qml item pointer to remove from sidebar

**description**
: call a qml function that remove item from left sidebar

---
#### void removeFromRightContainer(QQuickItem *item);

**parameters**
:
  - **item**: qml item pointer to remove from sidebar

**description**
: call a qml function that remove item from right sidebar

---
#### void showListWindow();

**parameters**
:

**description**
: toggle the mListWindow between show & hide

---
#### void setListWindow(ListWindow *listWindow);

**parameters**
:
  - **listWindow**: new for setting mListWindow

**description**
: setter for mListWindow

---
#### bool event(QEvent *ev) override;

**parameters**
:
  - **ev**: (?)

**description**
: (?)

---
#### void showInfoItem(QQuickItem* item, QString title);

**parameters**
:
  - **item**: (?)
  - **title**: (?)

**description**
: (?)

---
#### void hideInfoItem(QQuickItem* item);

**parameters**
:
  - **item**: (?)

**description**
: (?)

---
#### void hideProperty(QQuickItem* item);

**parameters**
:
  - **item**: (?)

**description**
: (?)

---
#### void addTabToListWindow(const QString tabTitle, QQuickItem *tabItem);

**parameters**
:
  - **tabTitle**: (?)
  - **tabItem**: (?)

**description**
: (?)
