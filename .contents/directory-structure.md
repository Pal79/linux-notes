<h1 align="center">Könyvtárszerkezet</h1>
<hr/>
<table>
    <thead>
        <tr>
            <th>könyvtár</th>
            <th>Leírás</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>/</td>
            <td>A hierarchikus könyvtárfa kiindulópontja (gyökér könyvtár)</td>
        </tr>
        <tr>
            <td>/boot</td>
            <td>A rendszer indításához szükséges állományok helye (grub, vmlinuz, stb)</td>
        </tr>
        <tr>
            <td>/bin</td>
            <td>A futtatható parancsok könyvtára -binaries</td>
        </tr>
        <tr>
            <td>/sbin</td>
            <td>A rendszergazda parancsai -superuser bin</td>
        </tr>
        <tr>
            <td>/lib</td>
            <td>Az induláshoz szükséges osztott rendszerkönyvtárak -libraries<br/>Továbbá tartalmazza a rendszerhez csatolható modulokat, meghajtóprogramokat</td>
        </tr>
        <tr>
            <td>/dev</td>
            <td>A rendszerhez csatlakozott, csatolható különleges állományok -devices</td>
        </tr>
        <tr>
            <td>/etc</td>
            <td>Beállítófájlok, helyi indító parancsok, jelszavak, hálózati-beállítók, etc. helye.</td>
        </tr>
        <tr>
            <td>/home</td>
            <td>Minden felhasználó saját könyvtára itt foglal helyet. (Otthon, édes otthon)</td>
        </tr>
        <tr>
            <td>/mnt</td>
            <td>A felcsatolt (mountolt) perifériák könyvtára. -mount</td>
        </tr>
        <tr>
            <td>/proc</td>
            <td>Itt látható, ahogy a rendszer "él". -process information<br/>Érdemes tüzetesebben átnézni, hiszen érdekes dolgokat találhatunk itt.<br/>pl.: /proc/cpuinfo fájl kiíratásával információt kaphatsz processzorodról.</td>
        </tr>
        <tr>
            <td>/root</td>
            <td>A rendszer gazdájának könyvtára.</td>
        </tr>
        <tr>
            <td>/tmp</td>
            <td>Ideiglenes adatok tárolására használt könyvtár. -temp</td>
        </tr>
        <tr>
            <td>/usr</td>
            <td>Alkalmazások, rendszereszközök tömkelege, a legforgalmasabb könytár. (pl X Window)</td>
        </tr>
        <tr>
            <td>/var</td>
            <td>Változó adatokat tartalmazó állományok könyvtára. /pl.: nyomtatási munkák, levelek, etc)<br/>/var/log : napló fájlok, különös jelentőséggel bírnak a rendszer biztonságának szempontjából</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="2">
                <a href="../README.md">Vissza</a>
            </td>
        </tr>
    </tfoot>
</table>