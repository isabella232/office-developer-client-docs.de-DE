---
title: DBEngine.DefaultType Property (DAO)
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
ms.openlocfilehash: d32c0860f76aeeaa64a060a55579d05c1eb571ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474621"
---
# <a name="dbenginedefaulttype-property-dao"></a>DBEngine.DefaultType Property (DAO)


**Betrifft**: Access 2013 | Office 2013

Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der den beim Erstellen des nächsten **[Workspace](workspace-object-dao.md)** -Objekts verwendeten Typ des Arbeitsbereichs angibt.

## <a name="syntax"></a>Syntax

*Ausdruck* . DefaultType

*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung oder der Rückgabewert kann eine der **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)** -Konstanten sein.


> [!NOTE]
> <P>[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</P>



Die Einstellung kann für ein einzelnes **Workspace** überschrieben werden, indem das Argument Type auf die **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** -Methode.

