---
title: Catalog-Objekt (ADO MD)
TOCTitle: Catalog object (ADO MD)
ms:assetid: 708c4082-3589-7f3b-5ea3-f3705f3d3ff1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249445(v=office.15)
ms:contentKeyID: 48545559
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ee7d2e68df90c8eee4227f949f93ea074b7df97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296591"
---
# <a name="catalog-object-ado-md"></a>Catalog-Objekt (ADO MD)


**Gilt für**: Access 2013, Office 2013

Enthält multidimensionale Schemainformationen (Cubes und zugrunde liegende Dimensionen, Hierarchien, Ebenen und Elemente), die für einen multidimensionalen Datenanbieter (Datenprovider, MDP) spezifisch sind.

## <a name="remarks"></a>Bemerkungen

Die Auflistungen und Eigenschaften eines **Catalog**-Objekts ermöglichen Folgendes:

- Öffnen des Katalogs, indem Sie für die [ActiveConnection](activeconnection-property-ado-md.md)-Eigenschaft ein [Connection](connection-object-ado.md)-ADO-Standardobjekt oder eine gültige Verbindungszeichenfolge festlegen.

- Identify the **Catalog** with the [Name](name-property-ado-md.md) property.

- Durchlaufen der Cubes in einem Katalog, indem Sie die [CubeDefs](cubedefs-collection-ado-md.md)-Auflistung verwenden.

