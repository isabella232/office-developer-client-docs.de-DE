---
<<<<<<< HEAD-Titel: Status-Eigenschaft (ADO) TOCTitle: Status-Eigenschaft (ADO) === Titel: State-Eigenschaft (ADO) TOCTitle: State-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15) Ms:contentKeyID: 48547053 ms.date: 09/18/2015 Mtps_version: Office. 15 f1_keywords:
- ado210.chm1231176 f1_categories:
- Office.Version=v15
---

<<<<<<< Kopf
# <a name="state-property-ado"></a>State-Eigenschaft (ADO)
=======
# <a name="state-property-ado"></a>State-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt für alle entsprechenden Objekte an, ob deren Status als geöffnet oder geschlossen gilt.

Gibt für alle entsprechenden Objekte, die eine asynchrone Methode ausführen, den aktuellen Status des Objekts an: Verbindungsherstellung (connecting), Ausführen (executing) oder Abrufen (retrieving).

<<<<<<< Kopf
## <a name="return-value"></a>Rückgabewert
=======
## <a name="return-value"></a>Rückgabewert
>>>>>>> master

Gibt einen **Long** -Wert zurück, bei dem es sich um einen [ObjectStateEnum](objectstateenum.md)-Wert handeln kann. Der Standardwert ist **adStateClosed**.

## <a name="remarks"></a>Hinweise

Mit der **State** -Eigenschaft können Sie jederzeit den aktuellen Status eines bestimmten Objekts ermitteln.

Die **State** -Eigenschaft des Objekts kann kombinierte Werte besitzen. Wenn beispielsweise eine Anweisung ausgeführt wird, besitzt die Eigenschaft einen aus **adStateOpen** und **adStateExecuting** bestehenden kombinierten Wert.

Die **State** -Eigenschaft ist schreibgeschützt.

