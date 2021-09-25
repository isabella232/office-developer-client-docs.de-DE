---
title: ParentURL-Eigenschaft (ADO)
TOCTitle: ParentURL property (ADO)
ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15)
ms:contentKeyID: 48548517
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 17d65b4b471172d08ce5868e78d43c8b101f1476
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617874"
---
# <a name="parenturl-property-ado"></a>ParentURL-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Eine absolute URL-Zeichenfolge wird angegeben, die auf das übergeordnete [Record](record-object-ado.md)-Objekt des aktuellen **Record**-Objekts zeigt.

## <a name="return-value"></a>Rückgabewert

Gibt einen **String**-Wert zurück, der die URL des übergeordneten **Record**-Objekts angibt.

## <a name="remarks"></a>Bemerkungen

Die **ParentURL**-Eigenschaft hängt von der Quelle ab, die zum Öffnen des **Record**-Objekts verwendet wird. Das **Record**-Objekt kann beispielsweise mit einer Quelle geöffnet werden, die einen relativen Pfadnamen eines Verzeichnisses enthält, auf das von der [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft verwiesen wird.

Angenommen, "second" ist ein Ordner, der unter "first" enthalten ist. Öffnen Sie das **Record** -Objekt folgendermaßen:

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

Jetzt ist der Wert der **ParentURL -Eigenschaft** **ParentURL** -Eigenschaft " https://first " ist, identisch mit **ActiveConnection**.

Die Quelle kann auch eine absolute URL sein, z. B. " https://first/second . The **ParentURL** property is then " https://first " , the level above . The **ParentURL** property is then " https://first " , the level above "second" .

Diese Eigenschaft kann in den folgenden Fällen ein Nullwert sein:

- Für das aktuelle Objekt gibt es kein übergeordnetes Objekt. Beispiel: Wenn das **Record**-Objekt den Stamm eines Verzeichnisses darstellt.

- Das **Record**-Objekt stellt eine Entität dar, die mit einer URL nicht angegeben werden kann.

Die Eigenschaft ist schreibgeschützt.


> [!NOTE]
> - Diese Eigenschaft wird nur von Dokumentquellenanbietern wie z. B. [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) unterstützt. Weitere Informationen finden Sie unter [Datensätze und vom Anbieter bereitgestellte Felder](records-and-provider-supplied-fields.md).
> - Bei URLs, die das HTTP-Schema verwenden, wird automatisch der Microsoft OLE DB-Anbieter für Internet Publishing aufgerufen. Weitere Informationen finden Sie unter [Absolute und relative URLs](absolute-and-relative-urls.md). 
> - Enthält der aktuelle Datensatz einen Datensatz aus einem ADO-**Recordset**-Objekt, verursacht der Zugriff auf die **ParentURL**-Eigenschaft einen Laufzeitfehler, der angibt, dass keine URL möglich ist.


