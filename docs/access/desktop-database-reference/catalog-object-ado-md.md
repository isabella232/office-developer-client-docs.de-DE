---
title: Catalog-Objekt (ADO MD)
TOCTitle: Catalog object (ADO MD)
ms:assetid: 708c4082-3589-7f3b-5ea3-f3705f3d3ff1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249445(v=office.15)
ms:contentKeyID: 48545559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c7d7c1aac77ff44f253c45c793a61737111dd4a0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553221"
---
# <a name="catalog-object-ado-md"></a>Catalog-Objekt (ADO MD)


**Gilt für**: Access 2013, Office 2013

Enthält multidimensionale Schemainformationen (Cubes und zugrunde liegende Dimensionen, Hierarchien, Ebenen und Elemente), die für einen multidimensionalen Datenanbieter (Datenprovider, MDP) spezifisch sind.

## <a name="remarks"></a>HinwBemerkungeneise

Die Auflistungen und Eigenschaften eines **Catalog**-Objekts ermöglichen Folgendes:

- Öffnen des Katalogs, indem Sie für die [ActiveConnection](activeconnection-property-ado-md.md)-Eigenschaft ein [Connection](connection-object-ado.md)-ADO-Standardobjekt oder eine gültige Verbindungszeichenfolge festlegen.

- Identify the **Catalog** with the [Name](name-property-ado-md.md) property.

- Durchlaufen der Cubes in einem Katalog, indem Sie die [CubeDefs](cubedefs-collection-ado-md.md)-Auflistung verwenden.

