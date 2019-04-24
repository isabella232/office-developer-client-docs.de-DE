---
title: DbEngine. DefaultType-Eigenschaft (DAO)
TOCTitle: DefaultType Property
ms:assetid: b4371f3e-1ce0-1d0f-93a8-0c5329b510ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822060(v=office.15)
ms:contentKeyID: 48547217
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053580
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 23f6c87ede6da2cc5b2f3203bfa13cb17bf93e82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294379"
---
# <a name="dbenginedefaulttype-property-dao"></a>DbEngine. DefaultType-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der den beim Erstellen des nächsten **[Workspace](workspace-object-dao.md)** -Objekts verwendeten Typ des Arbeitsbereichs angibt.

## <a name="syntax"></a>Syntax

*Ausdruck* . DefaultType

*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung oder der Rückgabewert kann eine der **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)** -Konstanten sein.


> [!NOTE]
> [!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.

Die Einstellung kann für einen einzelnen **Arbeitsbereich** außer Kraft gesetzt werden, indem das Argument **[](dbengine-createworkspace-method-dao.md)** Type auf die CreateWorkspace-Methode festgelegt wird.

