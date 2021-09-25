---
title: QueryDef.CacheSize-Eigenschaft (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 07ccd63bab2b7303b97063e163ad838ac2d37d44
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558065"
---
# <a name="querydefcachesize-property-dao"></a>QueryDef.CacheSize-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Legt die Anzahl der von einer ODBC-Datenquelle abgefragten Datensätze fest, die lokal zwischengespeichert werden, oder gibt den betreffenden Wert zurück. **Long**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . Cachesize

*Ausdruck* Eine Variable, die ein **QueryDef**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow. A typical value is 100. A setting of 0 turns off caching.

Das Microsoft Access-Datenbankmodul fordert Datensätze innerhalb des Cachebereichs aus dem Cache an, und es fordert Datensätze außerhalb des Cachebereichs vom Server an.

Aus dem Cache abgerufene Datensätze enthalten keine Änderungen, die andere Benutzer gleichzeitig an den Quelldaten vorgenommen haben.

