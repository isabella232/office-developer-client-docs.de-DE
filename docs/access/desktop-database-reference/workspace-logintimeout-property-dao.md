---
title: Workspace. LoginTimeout-Eigenschaft (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 5f03b166-abbc-20de-1a01-3869a9f2907d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194743(v=office.15)
ms:contentKeyID: 48545151
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbc0ed4849e8c22bc7023bd4254fdee74a5d016c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306909"
---
# <a name="workspacelogintimeout-property-dao"></a>Workspace. LoginTimeout-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Legt fest, wie viele Sekunden gewartet wird, bis ein Fehler auftritt, wenn versucht wird, sich bei einer ODBC-Datenbank anzumelden, oder gibt die betreffende Anzahl von Sekunden zurück.

## <a name="syntax"></a>Syntax

*Ausdruck* . LoginTimeout

*Ausdruck* Eine Variable, die ein **Workspace** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

The default **LoginTimeout** property setting is 20 seconds. When the **LoginTimeout** property is set to 0, no timeout occurs.

Wenn Sie versuchen, sich bei einer ODBC-Datenbank anzumelden, wie etwa bei Microsoft SQL Server, kann die Verbindung aufgrund eines Netzwerkfehlers fehlschlagen oder aber weil der Server nicht ausgeführt wird. Anstatt die standardmäßig festgelegten 20 Sekunden auf die Verbindung zu warten, können Sie festlegen, wie lange gewartet werden soll, bis ein Fehler erzeugt wird. Die Anmeldung beim Server wird implizit als Teil einer Reihe von verschiedenen Ereignissen ausgeführt, wie etwa beim Ausführen einer Abfrage einer externen Serverdatenbank.

