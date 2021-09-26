---
title: Database.Synchronize-Methode (DAO)
TOCTitle: Synchronize Method
ms:assetid: 5e716a4a-2430-8106-5c34-a02dd28bc4f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194659(v=office.15)
ms:contentKeyID: 48545137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053357
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 8c12d87cd9d5730c8e64add44254bc429256e741
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589764"
---
# <a name="databasesynchronize-method-dao"></a>Database.Synchronize-Methode (DAO)


**Gilt für**: Access 2013, Office 2013

Synchronisiert zwei Replikate (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . Synchronize(***DbPathName** _, _*_ExchangeType_**)

*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.

## <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich/optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>DbPathName</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Der Pfad zum Zielreplikat, mit dem die Datenbank synchronisiert wird.</p></td>
</tr>
<tr class="even">
<td><p><em>Exchangetype</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> -Konstante, die angibt, in welche Richtung Änderungen zwischen den beiden Datenbanken synchronisiert werden sollen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

Mit **Synchronize** können Sie Daten und Entwurfsänderungen zwischen zwei Datenbanken austauschen. Entwurfsänderungen werden grundsätzlich zuerst vorgenommen. Beide Datenbanken müssen sich auf derselben Entwurfsebene befinden, damit Daten ausgetauscht werden können. Beispielsweise kann ein Austausch vom Typ **dbRepExportChanges** Entwurfsänderungen an einem Replikat verursachen, obwohl Datenänderungen nur von der Datenbank zu DbPathName fließen.

Das in DbPathName identifizierte Replikat muss Teil derselben Replikatgruppe sein. Wenn beide Replikate über dieselbe **ReplicaID**-Eigenschafteneinstellung verfügen oder Designmaster für zwei verschiedene Replikatgruppen sind, schlägt die Synchronisierung fehl.

Verwenden Sie die **dbRepSyncInternet**-Konstante, um zwei Replikate über das Internet zu synchronisieren. In diesem Fall geben Sie eine URL-Adresse (Uniform Resource Locator) für das Argument DbPathName an, anstatt einen lokalen Netzwerkpfad anzugeben.


> [!NOTE]
> [!HINWEIS] Es ist nicht möglich, Teilreplikate mit anderen Teilreplikaten zu synchronisieren. Weitere Informationen erhalten Sie im Thema zur [PopulatePartial](database-populatepartial-method-dao.md) -Methode.


