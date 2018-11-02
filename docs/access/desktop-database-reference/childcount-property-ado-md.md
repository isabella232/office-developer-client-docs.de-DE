---
title: ChildCount-Eigenschaft (ADO MD)
TOCTitle: ChildCount property (ADO MD)
ms:assetid: ff1872f0-d5f6-174e-0473-7997a462ca81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250309(v=office.15)
ms:contentKeyID: 48548956
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8a55f54bfe796f9dfa0fc3ec157c8f7cfe9fa11
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925219"
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

