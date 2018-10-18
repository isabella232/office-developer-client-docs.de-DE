---
<<<<<<< HEAD-Titel: Direction-Eigenschaft (ADO) TOCTitle: Direction-Eigenschaft (ADO) === Titel: Direction-Eigenschaft (ADO) TOCTitle: Direction-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15) Ms:contentKeyID: 48544823 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="direction-property-ado"></a>Direction-Eigenschaft (ADO)
=======
# <a name="direction-property-ado"></a>Direction-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt an, ob der [Parameter](parameter-object-ado.md) einen Eingabeparameter, einen Ausgabeparameter oder einen Ein- und Ausgabeparameter darstellt, oder ob der Parameter der Rückgabewert aus einer gespeicherten Prozedur ist.

<<<<<<< Kopf
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
=======
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
>>>>>>> master

Mit dieser Eigenschaft wird ein [ParameterDirectionEnum](parameterdirectionenum.md)-Wert festgelegt oder zurückgegeben.

## <a name="remarks"></a>Hinweise

Mit der **Direction** -Eigenschaft geben Sie an, wie ein Parameter an eine oder aus einer Prozedur übergeben wird. Die **Direction** -Eigenschaft bietet Lese-/Schreibzugriff. Dadurch können Sie Anbieter verwenden, die diese Informationen nicht zurückgeben, oder Sie können diese Informationen festlegen, wenn ADO den Anbieter nicht extra aufrufen soll, um Parameterinformationen abzurufen.

Nicht alle Anbieter können die Richtung von Parametern in ihren gespeicherten Prozeduren bestimmen. In diesen Fällen müssen Sie die **Direction** -Eigenschaft festlegen, bevor Sie die Abfrage ausführen.

