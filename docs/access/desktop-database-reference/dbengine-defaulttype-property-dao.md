---
title: DBEngine.DefaultType-Eigenschaft (DAO)
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
ms.localizationpriority: medium
ms.openlocfilehash: 619d46e493f45745d47a9bb8188df8dfe240c3ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59632077"
---
# <a name="dbenginedefaulttype-property-dao"></a>DBEngine.DefaultType-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der den beim Erstellen des nächsten **[Workspace](workspace-object-dao.md)** -Objekts verwendeten Typ des Arbeitsbereichs angibt.

## <a name="syntax"></a>Syntax

*Ausdruck* . Defaulttype

*Ausdruck* Eine Variable, die ein **DBEngine**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung oder der Rückgabewert kann eine der **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)** -Konstanten sein.


> [!NOTE]
> ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.

Die Einstellung kann für einen einzelnen **Arbeitsbereich** überschrieben werden, indem das Typargument auf die **[CreateWorkspace-Methode](dbengine-createworkspace-method-dao.md)** festgelegt wird.

