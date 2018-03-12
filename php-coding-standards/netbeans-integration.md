### Integrating PHPCS with Netbeans 8

#### Configuring CodeSniffer in NetBeans
 * Go to Netbeans `Tools > Options > PHP > Code Analysis`
 * Code Sniffer: Browse to `phpcs` executable file. Then wait for `Default Standard` list to be loaded
 * Default Standard: Choose `Wordpress`
 * Click `OK`
 ![Tools > Options > PHP > Code Analysis](https://github.com/truonglv-eva/coding-rule/blob/master/images/netbean-phpcs-integration-plugin.jpg?raw=true)
 
 If all goes well you will see something like below in your netbeans output window:
![Netbeans output window](https://github.com/truonglv-eva/coding-rule/blob/master/images/NetBeans-phpCS-window.png?raw=true)

#### Running CodeSniffer in NetBeans

 Select a file or a folder. Then click `Source >> Inspect` Menu
![Source >> Inspect Menu](https://github.com/truonglv-eva/coding-rule/blob/master/images/netbeans-run-codensiffer-1.png?raw=true)

 Then select Code Sniffer configuration from drop-down and hit `Inspect` button
![Code Sniffer configuration >> Inspect](https://github.com/truonglv-eva/coding-rule/blob/master/images/Condesniffer-run-in-netbeans.png?raw=true)
