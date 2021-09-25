---
title: Database.Version-Eigenschaft (DAO)
TOCTitle: Version Property
ms:assetid: 40faaa0c-e764-e968-f606-7e06ded80c3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192887(v=office.15)
ms:contentKeyID: 48544440
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ea3d061025619ec2368b1cc3c732c82b2f291ba4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581546"
---
# <a name="databaseversion-property-dao"></a>Database.Version-Eigenschaft (DAO)

**Gilt für**: Access 2013, Office 2013

In einem Microsoft Access-Arbeitsbereich gibt diese Eigenschaft die Version der Microsoft Jet- oder Microsoft Access-Datenbank-Engine zurück, mit der die Datenbank erstellt wurde. Schreibgeschützter **String**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . Version

*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.

## <a name="remarks"></a>HinwBemerkungeneise

Der Rückgabewert ist ein String-Datentyp, der als Versionsnummer im folgenden Format ausgewertet wird.

- Der Microsoft Access-Arbeitsbereich stellt die Versionsnummer im Format *"major.minor"* dar. For example, "3.0". The product version number consists of the version number (3), a period, and the release number (0).

Die folgende Tabelle zeigt, welche Version der Datenbank-Engine in verschiedenen Versionen von Microsoft-Produkten enthalten waren.

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Datenbank-Engine</p></th>
<th><p>Version (Freigabejahr)</p></th>
<th><p>Microsoft Access</p></th>
<th><p>Microsoft Visual Basic</p></th>
<th><p>Microsoft Excel</p></th>
<th><p>Microsoft Visual C++</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>1.0 (1992)</p></td>
<td><p>1.0</p></td>
<td><p>Nicht zutreffend</p></td>
<td><p>Nicht zutreffend</p></td>
<td><p>Nicht zutreffend</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Jet</p></td>
<td><p>1.1 (1993)</p></td>
<td><p>1.1</p></td>
<td><p>3.0</p></td>
<td><p>Nicht zutreffend</p></td>
<td><p>Nicht zutreffend</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>2.0 (1994)</p></td>
<td><p>2.0</p></td>
<td><p>Nicht zutreffend</p></td>
<td><p>Nicht zutreffend</p></td>
<td><p>Nicht zutreffend</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Jet</p></td>
<td><p>2.5 (1995)</p></td>
<td><p>Nicht zutreffend</p></td>
<td><p>4.0 (16-Bit)</p></td>
<td><p>Nicht zutreffend</p></td>
<td><p>Nicht zutreffend</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>3.0 (1995)</p></td>
<td><p>‘ 95 (7.0)’</p></td>
<td><p>4.0 (32-Bit)</p></td>
<td><p>‘ 95 (7.0)’</p></td>
<td><p>4.x</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Jet</p></td>
<td><p>3.5 (1996)</p></td>
<td><p>‘ 97 (8.0)’</p></td>
<td><p>5.0</p></td>
<td><p>‘ 97 (8.0)’</p></td>
<td><p>5.0</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Jet</p></td>
<td><p>4.0 (2000)</p></td>
<td><p>2000 (9.0)</p></td>
<td><p></p></td>
<td><p>2000 (9.0)</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Microsoft Access-Datenbank-Engine</p></td>
<td><p>12.0 (2007)</p></td>
<td><p>2007</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

