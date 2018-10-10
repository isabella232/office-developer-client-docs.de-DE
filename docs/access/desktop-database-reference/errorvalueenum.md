---
title: ErrorValueEnum (Access PC-Datenbank-Referenz)
TOCTitle: ErrorValueEnum
ms:assetid: 2af99f32-6004-1225-367c-45d693f447b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249058(v=office.15)
ms:contentKeyID: 48543921
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de7f19c119c3161ece57344b911fcca36a1a8a3d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474559"
---
# <a name="errorvalueenum"></a>ErrorValueEnum


**Betrifft**: Access 2013 | Office 2013

Gibt den Typ des ADO-Laufzeitfehlers an.

Es werden drei Fehlernummerntypen aufgeführt:

  - Positive Dezimalzahl - die niedrigen zwei Bytes der vollständigen Zahl im Dezimalstellenformat. Diese Nummer wird im Standard-Fehlermeldungsdialogfeld von Visual Basic angezeigt. Zum Beispiel Laufzeitfehler "3707".

  - Negative Dezimalzahl - die Dezimalübersetzung der vollständigen Fehlernummer.

  - Hexadezimal – die hexadezimale Darstellung der vollständigen Fehlernummer. Der Windows-Einrichtungscode befindet sich in der vierten Ziffer. *A* ist der Einrichtungscode für ADO-Fehlernummern. Beispielsweise: 0x800 ***A*** 0E7B.


> [!NOTE]
> <P>OLE DB-Fehler können an Ihre ADO-Anwendung übergeben werden. Diese können in der Regel von einem Windows-Einrichtungscode von <EM>4</EM> identifiziert werden. Beispielsweise 0x800 <STRONG><EM>4</EM></STRONG>.... Weitere Informationen zu diesen Nummern finden Sie in Kapitel 16 der <EM>OLE DB Programmer's Reference</EM>.</P>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adErrBoundToCommand</strong></p></td>
<td><p>3707<br />
-2146824581<br />
0x800A0E7B</p></td>
<td><p>Kann die <strong>ActiveConnection</strong>-Eigenschaft eines <strong>Recordset</strong>-Objekts nicht ändern, das als Quelle ein <strong>Command</strong>-Objekt besitzt.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrCannotComplete</strong></p></td>
<td><p>3732<br />
-2146824556<br />
0x800A0E94</p></td>
<td><p>Server kann den Vorgang nicht abschließen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrCantChangeConnection</strong></p></td>
<td><p>3748<br />
-2146824540<br />
0x800A0EA4</p></td>
<td><p>Verbindung wurde verweigert. Die von Ihnen angeforderte neue Verbindung weist andere Eigenschaften als die bereits verwendete auf.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrCantChangeProvider</strong></p></td>
<td><p>3220<br />
-2146825068<br />
0X800A0C94</p></td>
<td><p>Der bereitgestellte Anbieter unterscheidet sich von dem bereits verwendeten Anbieter.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrCantConvertvalue</strong></p></td>
<td><p>3724<br />
-2146824564<br />
0x800A0E8C</p></td>
<td><p>Der Datenwert kann aus anderen Gründen als einem Vorzeichenkonflikt oder einem Datenüberlauf nicht konvertiert werden. Beispielsweise könnten bei der Konvertierung Daten abgeschnitten werden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrCantCreate</strong></p></td>
<td><p>3725<br />
-2146824563<br />
0x800A0E8D</p></td>
<td><p>Der Datenwert kann nicht festgelegt oder abgerufen werden, da der Felddatentyp unbekannt war, oder der Anbieter verfügte über unzureichende Ressourcen zum Ausführen des Vorgangs.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrCatalogNotSet</strong></p></td>
<td><p>3747<br />
-2146824541<br />
0x800A0EA3</p></td>
<td><p>Für den Vorgang ist ein gültiger <strong>ParentCatalog</strong> erforderlich.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrColumnNotOnThisRow</strong></p></td>
<td><p>3726<br />
-2146824562<br />
0x800A0E8E</p></td>
<td><p>Der Datensatz enthält dieses Feld nicht.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrDataConversion</strong></p></td>
<td><p>3421<br />
-2146824867<br />
0x800A0D5D</p></td>
<td><p>Die Anwendung verwendet für den aktuellen Vorgang einen Wert des falschen Datentyps.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrDataOverflow</strong></p></td>
<td><p>3721<br />
-2146824567<br />
0x800A0E89</p></td>
<td><p>Der Datenwert ist zu groß, um vom Felddatentyp dargestellt zu werden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrDelResOutOfScope</strong></p></td>
<td><p>3738<br />
-2146824550<br />
0x800A0E9A</p></td>
<td><p>URL des zu löschenden Objekts befindet sich außerhalb des aktuellen Datensatzes.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrDenyNotSupported</strong></p></td>
<td><p>3750<br />
-2146824538<br />
0x800A0EA6</p></td>
<td><p>Der Anbieter unterstützt Freigabeeinschränkungen nicht.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrDenyTypeNotSupported</strong></p></td>
<td><p>3751<br />
-2146824537<br />
0x800A0EA7</p></td>
<td><p>Der Anbieter unterstützt die angeforderte Art von Freigabeeinschränkung nicht.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrFeatureNotAvailable</strong></p></td>
<td><p>3251<br />
-2146825037<br />
0x800A0CB3</p></td>
<td><p>Objekt oder Anbieter kann den angeforderten Vorgang nicht ausführen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrFieldsUpdateFailed</strong></p></td>
<td><p>3749<br />
-2146824539<br />
0x800A0EA5</p></td>
<td><p>Feldaktualisierung schlug fehl. Überprüfen Sie die <strong>Status</strong>-Eigenschaft der einzelnen Feldobjekte, um weitere Informationen zu erhalten.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrIllegalOperation</strong></p></td>
<td><p>3219<br />
-2146825069<br />
0x800A0C93</p></td>
<td><p>Der Vorgang ist in diesem Zusammenhang nicht zulässig.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrIntegrityViolation</strong></p></td>
<td><p>3719<br />
-2146824569<br />
0x800A0E87</p></td>
<td><p>Der Datenwert steht in Konflikt mit den Integritätseinschränkungen des Felds.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrInTransaction</strong></p></td>
<td><p>3246<br />
-2146825042<br />
0x800A0CAE</p></td>
<td><p>Das <strong>Connection</strong> -Objekt kann während einer Transaktion nicht explizit geschlossen werden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrInvalidArgument</strong></p></td>
<td><p>3001<br />
-2146825287<br />
0x800A0BB9</p></td>
<td><p>Argumente weisen den falschen Typ auf, liegen außerhalb des gültigen Bereichs oder stehen miteinander in Konflikt.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrInvalidConnection</strong></p></td>
<td><p>3709<br />
-2146824579<br />
0x800A0E7D</p></td>
<td><p>Die Verbindung kann nicht für diesen Vorgang verwendet werden. Die Verbindung ist entweder geschlossen oder in diesem Kontext ungültig.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrInvalidParamInfo</strong></p></td>
<td><p>3708<br />
-2146824580<br />
0x800A0E7C</p></td>
<td><p>Das <strong>Parameter</strong> -Objekt ist nicht ordnungsgemäß definiert. Inkonsistente oder unvollständige Informationen wurden eingegeben.  </p></td>
</tr>
<tr class="even">
<td><p><strong>adErrInvalidTransaction</strong></p></td>
<td><p>3714<br />
-2146824574<br />
0x800A0E82</p></td>
<td><p>Die Koordinierungstransaktion ist ungültig oder wurde nicht gestartet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrInvalidURL</strong></p></td>
<td><p>3729<br />
-2146824559<br />
0x800A0E91</p></td>
<td><p>URL enthält ungültige Zeichen. Stellen Sie sicher, dass die URL fehlerfrei eingegeben wird.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrItemNotFound</strong></p></td>
<td><p>3265<br />
-2146825023<br />
0x800A0CC1</p></td>
<td><p>Das Element, das dem angeforderten Namen oder der angeforderten Zahl entspricht, wurde in der Auflistung nicht gefunden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrNoCurrentRecord</strong></p></td>
<td><p>3021<br />
-2146825267<br />
0x800A0BCD</p></td>
<td><p><strong>BOF</strong> oder <strong>EOF</strong> ist Wahr bzw. der aktuelle Datensatz wurde gelöscht. Für den angeforderten Vorgang ist ein aktueller Datensatz erforderlich.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrNotExecuting</strong></p></td>
<td><p>3715<br />
-2146824573<br />
0x800A0E83</p></td>
<td><p>Der Vorgang kann nicht verarbeitet werden, wenn er nicht ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrNotReentrant</strong></p></td>
<td><p>3710<br />
-2146824578<br />
0x800A0E7E</p></td>
<td><p>Der Vorgang kann während der Verarbeitung des Ereignisses nicht ausgeführt werden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrObjectClosed</strong></p></td>
<td><p>3704<br />
-2146824584<br />
0x800A0E78</p></td>
<td><p>Der Vorgang ist nicht zulässig, wenn das Objekt geschlossen ist.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrObjectInCollection</strong></p></td>
<td><p>3367<br />
-2146824921<br />
0x800A0D27</p></td>
<td><p>Objekt befindet sich bereits in der Auflistung. Anfügen nicht möglich.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrObjectNotSet</strong></p></td>
<td><p>3420<br />
-2146824868<br />
0x800A0D5C</p></td>
<td><p>Das Objekt ist nicht mehr gültig.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrObjectOpen</strong></p></td>
<td><p>3705<br />
-2146824583<br />
0x800A0E79</p></td>
<td><p>Der Vorgang ist nicht zulässig, wenn das Objekt geöffnet ist.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrOpeningFile</strong></p></td>
<td><p>3002<br />
-2146825286<br />
0x800A0BBA</p></td>
<td><p>Die Datei konnte nicht geöffnet werden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrOperationCancelled</strong></p></td>
<td><p>3712<br />
-2146824576<br />
0x800A0E80</p></td>
<td><p>Vorgang wurde vom Benutzer abgebrochen.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrOutOfSpace</strong></p></td>
<td><p>3734<br />
-2146824554<br />
0x800A0E96</p></td>
<td><p>Vorgang kann nicht ausgeführt werden. Anbieter kann nicht genügend Speicherplatz abrufen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrPermissionDenied</strong></p></td>
<td><p>3720<br />
-2146824568<br />
0x800A0E88</p></td>
<td><p>Unzureichende Berechtigung verhindert Schreiben im Feld.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrProviderFailed</strong></p></td>
<td><p>3000<br />
-2146825288<br />
0x800A0BB8</p></td>
<td><p>Der Anbieter konnte den angeforderten Vorgang nicht ausführen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrProviderNotFound</strong></p></td>
<td><p>3706<br />
-2146824582<br />
0x800A0E7A</p></td>
<td><p>Anbieter kann nicht gefunden werden. Er ist möglicherweise nicht ordnungsgemäß installiert.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrReadFile</strong></p></td>
<td><p>3003<br />
-2146825285<br />
0x800A0BBB</p></td>
<td><p>Die Datei konnte nicht gelesen werden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrResourceExists</strong></p></td>
<td><p>3731<br />
-2146824557<br />
0x800A0E93</p></td>
<td><p>Kopiervorgang kann nicht ausgeführt werden. Von Ziel-URL benanntes Objekt ist bereits vorhanden. Geben Sie <strong>AdCopyOverwrite</strong> an, um das Objekt zu ersetzen.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrResourceLocked</strong></p></td>
<td><p>3730<br />
-2146824558<br />
0x800A0E92</p></td>
<td><p>Objekt, das von der angegebenen URL dargestellt wird, wurde von mindestens einem Prozess gesperrt. Warten Sie, bis der Prozess abgeschlossen ist, und versuchen Sie dann, den Vorgang erneut auszuführen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrResourceOutOfScope</strong></p></td>
<td><p>3735<br />
-2146824553<br />
0x800A0E97</p></td>
<td><p>Die Quell- oder Ziel-URL liegt außerhalb des Bereichs des aktuellen Datensatzes.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrSchemaViolation</strong></p></td>
<td><p>3722<br />
-2146824566<br />
0x800A0E8A</p></td>
<td><p>Der Datenwert steht in Konflikt mit dem Datentyp oder mit Einschränkungen des Felds.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrSignMismatch</strong></p></td>
<td><p>3723<br />
-2146824565<br />
0x800A0E8B</p></td>
<td><p>Fehler bei der Konvertierung, da der Datenwert ein Vorzeichen hat, der vom Anbieter verwendete Felddatentyp aber kein Vorzeichen aufweist.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrStillConnecting</strong></p></td>
<td><p>3713<br />
-2146824575<br />
0x800A0E81</p></td>
<td><p>Vorgang kann beim asynchronen Verbinden nicht ausgeführt werden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrStillExecuting</strong></p></td>
<td><p>3711<br />
-2146824577<br />
0x800A0E7F</p></td>
<td><p>Der Vorgang kann im asynchronen Modus nicht ausgeführt werden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrTreePermissionDenied</strong></p></td>
<td><p>3728<br />
-2146824560<br />
0x800A0E90</p></td>
<td><p>Unzureichende Berechtigungen für den Zugriff auf die Struktur oder die Unterstruktur.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrUnavailable</strong></p></td>
<td><p>3736<br />
-2146824552<br />
0x800A0E98</p></td>
<td><p>Vorgang konnte nicht abgeschlossen werden und der Status ist nicht verfügbar. Das Feld ist möglicherweise nicht verfügbar oder der Vorgang wurde nicht ausgeführt.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrUnsafeOperation</strong></p></td>
<td><p>3716<br />
-2146824572<br />
0x800A0E84</p></td>
<td><p>Die Sicherheitseinstellungen dieses Computers lassen den Zugriff auf eine Datenquelle in einer anderen Domäne nicht zu.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrURLDoesNotExist</strong></p></td>
<td><p>3727<br />
-2146824561<br />
0x800A0E8F</p></td>
<td><p>Entweder die Quell-URL oder das übergeordnete Element der Ziel-URL ist nicht vorhanden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrURLNamedRowDoesNotExist</strong></p></td>
<td><p>3737<br />
-2146824551<br />
0x800A0E99</p></td>
<td><p>Der von dieser URL genannte Datensatz ist nicht vorhanden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrVolumeNotFound</strong></p></td>
<td><p>3733<br />
-2146824555<br />
0x800A0E95</p></td>
<td><p>Anbieter findet das von der URL angegebene Speichergerät nicht. Stellen Sie sicher, dass die URL in der richtigen Schreibweise eingegeben wird.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrWriteFile</strong></p></td>
<td><p>3004<br />
-2146825284<br />
0x800A0BBC</p></td>
<td><p>Fehler beim Schreiben in die Datei.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adWrnSecurityDialog</strong></p></td>
<td><p>3717<br />
-2146824571<br />
0x800A0E85</p></td>
<td><p>Nur für die interne Verwendung. Verwendung wird nicht empfohlen.</p></td>
</tr>
<tr class="even">
<td><p><strong>adWrnSecurityDialogHeader</strong></p></td>
<td><p>3718<br />
-2146824570<br />
0x800A0E86</p></td>
<td><p>Nur für die interne Verwendung. Verwendung wird nicht empfohlen.</p></td>
</tr>
</tbody>
</table>


**ADO/WFC-Entsprechung**

Paket: **com.ms.wfc.data**

Nur die folgenden Teilmengen von ADO/WFC-Entsprechungen sind definiert.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.BOUNDTOCOMMAND</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.DATACONVERSION</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.FEATURENOTAVAILABLE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.ILLEGALOPERATION</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.INTRANSACTION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.INVALIDARGUMENT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.INVALIDCONNECTION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.INVALIDPARAMINFO</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.ITEMNOTFOUND</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.NOCURRENTRECORD</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.NOTEXECUTING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.NOTREENTRANT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.OBJECTCLOSED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.OBJECTINCOLLECTION</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.OBJECTNOTSET</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.OBJECTOPEN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.OPERATIONCANCELLED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.PROVIDERNOTFOUND</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.STILLCONNECTING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.STILLEXECUTING</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.UNSAFEOPERATION</p></td>
</tr>
</tbody>
</table>

