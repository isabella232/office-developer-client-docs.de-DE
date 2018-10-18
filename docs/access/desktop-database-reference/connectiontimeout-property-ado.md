---
<<<<<<< HEAD-Titel: ConnectionTimeout-Eigenschaft (ADO) TOCTitle: ConnectionTimeout-Eigenschaft (ADO) === Titel: ConnectionTimeout-Eigenschaft (ADO) TOCTitle: ConnectionTimeout-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15) Ms:contentKeyID: 48548589 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="connectiontimeout-property-ado"></a>ConnectionTimeout-Eigenschaft (ADO)
=======
# <a name="connectiontimeout-property-ado"></a>ConnectionTimeout-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt an, wie lange beim Einrichten einer Verbindung gewartet wird, bis der Versuch beendet und ein Fehler generiert wird.

<<<<<<< Kopf
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
=======
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
>>>>>>> master

Mit dieser Eigenschaft wird ein Wert vom Datentyp Long festgelegt oder zurückgegeben, der angibt, wie viele Sekunden gewartet werden soll, bis die Verbindung geöffnet wird. Der Standard ist 15.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **ConnectionTimeout** -Eigenschaft für ein [Connection](connection-object-ado.md) -Objekt Wenn Verzögerungen von Datenverkehr oder fett Netzwerkserver verwenden es erforderlich machen, einen Verbindungsversuch zu verlassen. Wenn das von der Einstellung der **ConnectionTimeout** -Eigenschaft vor dem Öffnen der Verbindung verstrichen, tritt ein Fehler auf, und ADO bricht den Versuch ab. Wenn Sie die Eigenschaft auf 0 (null) festlegen, wartet ADO unbegrenzt, bis die Verbindung geöffnet wird. Stellen Sie sicher, dass der Anbieter, den Sie Code schreiben, die **ConnectionTimeout** -Funktionalität unterstützt.

Die **ConnectionTimeout** -Eigenschaft hat Lese-/Schreibzugriff, wenn die Verbindung geschlossen ist. Wenn die Verbindung geöffnet ist, ist sie schreibgeschützt.

