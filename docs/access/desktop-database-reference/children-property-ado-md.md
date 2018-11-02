---
title: Children-Eigenschaft (ADO MD)
TOCTitle: Children property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b93081c577a0d93d442706f231dace5e7865976
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927704"
---
# <a name="children-property-ado-md"></a>Children-Eigenschaft (ADO MD)


**Betrifft**: Access 2013, Office 2013

Gibt eine [Members](members-collection-ado-md.md)-Auflistung zurück, für die das aktuelle [Member](member-object-ado-md.md)-Objekt das übergeordnete Objekt (Hauptobjekt) in der Hierarchie ist.

## <a name="return-values"></a>Rückgabewerte

Gibt eine **Members** -Auflistung zurück und ist schreibgeschützt.

## <a name="remarks"></a>Hinweise

Die **Children** -Eigenschaft enthält eine **Members** -Auflistung, für die das aktuelle **Member** -Objekt das in der Hierarchie übergeordnete Objekt ist. **Member** -Objekte auf Blattebene haben keine untergeordneten Elemente in der **Members** -Auflistung. Diese Eigenschaft wird nur für **Member** -Objekte unterstützt, die zu einem [Level](level-object-ado-md.md)-Objekt gehören. Wenn auf diese Eigenschaft durch **Member** -Objekte verwiesen wird, die zu einem [Position](position-object-ado-md.md)-Objekt gehören, tritt ein Fehler auf.

