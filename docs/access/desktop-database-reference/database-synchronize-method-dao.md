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
ms.openlocfilehash: dc32087ad924a81eea5290d84ffb63dc4ad5e1ff
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999050"
---
# <a name="databasesynchronize-method-dao"></a>Database.Synchronize-Methode (DAO)


**Betrifft**: Access 2013, Office 2013

Synchronisiert zwei Replikate (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . Synchronisieren Sie (***DbPathName***, ***ExchangeType***)

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
<th><p>Erforderlich oder optional</p></th>
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
<td><p><em>ExchangeType</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong>-Konstante, die angibt, in welche Richtung Änderungen zwischen den beiden Datenbanken synchronisiert werden sollen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Mit **Synchronize** können Sie Daten und Entwurfsänderungen zwischen zwei Datenbanken austauschen. Entwurfsänderungen werden grundsätzlich zuerst vorgenommen. Beide Datenbanken müssen sich auf derselben Entwurfsebene befinden, damit Daten ausgetauscht werden können. Beispielsweise möglicherweise ein Austausch von Typ **DbRepExportChanges** Designänderungen bei einem Replikat, obwohl die Daten in DbPathName Fluss nur aus der Datenbank ändert.

DbPathName angegebene Replikat muss Teil derselben Replikatgruppe sein. Wenn beide Replikate über dieselbe **ReplicaID**-Eigenschafteneinstellung verfügen oder Designmaster für zwei verschiedene Replikatgruppen sind, schlägt die Synchronisierung fehl.

Verwenden Sie die **dbRepSyncInternet**-Konstante, um zwei Replikate über das Internet zu synchronisieren. In diesem Fall geben Sie eine Adresse Uniform Resource Locator (URL) für das Argument DbPathName anstelle von angeben eines Pfads lokales Netzwerk.


> [!NOTE]
> [!HINWEIS] Es ist nicht möglich, Teilreplikate mit anderen Teilreplikaten zu synchronisieren. Weitere Informationen erhalten Sie im Thema zur [PopulatePartial](database-populatepartial-method-dao.md) -Methode.


