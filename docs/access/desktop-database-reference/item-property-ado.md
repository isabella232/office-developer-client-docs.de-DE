---
<<<<<<< HEAD-Titel: Item-Eigenschaft (ADO) TOCTitle: Item-Eigenschaft (ADO) === Titel: Item-Eigenschaft (ADO) TOCTitle: Item-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15) Ms:contentKeyID: 48545767 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="item-property-ado"></a>Item-Eigenschaft (ADO)
=======
# <a name="item-property-ado"></a>Item-Eigenschaft (ADO)
>>>>>>> master

**Betrifft**: Access 2013 | Office 2013

Gibt ein bestimmtes Element einer Auflistung nach Name oder Ordnungszahl an.

## <a name="syntax"></a>Syntax

Legen Sie*Objekt* = *Auflistung*. Item (Index)

<<<<<<< Kopf
## <a name="return-value"></a>Rückgabewert
=======
## <a name="return-value"></a>Rückgabewert
>>>>>>> master

Gibt einen Objektverweis zurück.

## <a name="parameters"></a>Parameter

- *Index*

- Ein **Variant** -Ausdruck, der als Name oder Ordnungszahl eines Objekts in einer Auflistung ausgewertet wird.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **Item** -Eigenschaft, um ein bestimmtes Objekt in einer Auflistung zurückzugeben. Wenn das **Element** ein Objekt in der Auflistung entspricht dem *Index* -Argument nicht finden kann, tritt ein Fehler auf. Darüber hinaus unterstützen einige Sammlungen nicht benannte Objekte; für diese Auflistungen müssen Sie die Ordnungszahl Verweise verwenden.

Die **Item** -Eigenschaft ist die Standardeigenschaft für alle Auflistungen. Die folgenden Syntaxformen sind deshalb austauschbar:

```vb
    collection.Item (Index)
    collection (Index)
```
