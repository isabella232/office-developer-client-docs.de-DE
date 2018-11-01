---
title: ChildCount-Eigenschaft (ADO MD)
TOCTitle: ChildCount Property (ADO MD)
ms:assetid: ff1872f0-d5f6-174e-0473-7997a462ca81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250309(v=office.15)
ms:contentKeyID: 48548956
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0ac5e65356e7ee66cda864bffc983ae1d394825b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879606"
---
# <a name="childcount-property-ado-md"></a>ChildCount-Eigenschaft (ADO MD)


**Betrifft**: Access 2013, Office 2013

Gibt die Anzahl von Elementen an, für die das aktuelle [Member](member-object-ado-md.md)-Objekt das übergeordnete Objekt (Hauptobjekt) in einer Hierarchie ist.

## <a name="return-values"></a>Rückgabewerte

Gibt einen schreibgeschützten, ganzzahligen **Long** -Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **ChildCount** -Eigenschaft, um eine geschätzte Anzahl von untergeordneten Elementen eines **Member** -Objekts zurückzugeben. Die tatsächliche Anzahl von untergeordneten Elementen eines **Member** -Objekts kann durch die [Children](children-property-ado-md.md)-Eigenschaft zurückgegeben werden.

Für **Member** -Objekte aus einem [Position](position-object-ado-md.md)-Objekt beträgt die maximal zurückgegebene Anzahl 65536. Wenn die tatsächliche Anzahl untergeordneter Elemente den Wert 65536 überschreitet, bleibt der Rückgabewert 65536. Die Anwendung sollte eine **ChildCount** -Eigenschaft von 65536 als größer/gleich 65536 untergeordnete Elemente interpretieren.

Verwenden Sie für **Member** -Objekte aus einem [Level](level-object-ado-md.md)-Objekt die ADO-[Count](count-property-ado.md)-Auflistungseigenschaft für die **Children** -Auflistung, um die genaue Anzahl von untergeordneten Elementen zu bestimmen. Das Bestimmen der genauen Anzahl untergeordneter Elemente kann einige Zeit dauern, wenn die Anzahl von untergeordneten Elementen in der Auflistung groß ist.

