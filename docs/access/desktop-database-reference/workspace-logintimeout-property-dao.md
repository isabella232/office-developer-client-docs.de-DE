---
title: Workspace.LoginTimeout Property (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 5f03b166-abbc-20de-1a01-3869a9f2907d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194743(v=office.15)
ms:contentKeyID: 48545151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a051d0a6f580f661b8f16489b66cede064523e44
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868994"
---
# <a name="workspacelogintimeout-property-dao"></a>Workspace.LoginTimeout Property (DAO)


**Betrifft**: Access 2013, Office 2013

Legt fest, wie viele Sekunden gewartet wird, bis ein Fehler auftritt, wenn versucht wird, sich bei einer ODBC-Datenbank anzumelden, oder gibt die betreffende Anzahl von Sekunden zurück.

## <a name="syntax"></a>Syntax

*Ausdruck* . LoginTimeout

*Ausdruck* Eine Variable, die ein **Workspace** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die Standardeinstellung der LoginTimeout-Eigenschaft beträgt 20 Sekunden. Wenn die LoginTimeout-Eigenschaft auf 0 gesetzt ist, tritt kein Timeout ein.

Wenn Sie versuchen, sich bei einer ODBC-Datenbank anzumelden, wie etwa bei Microsoft SQL Server, kann die Verbindung aufgrund eines Netzwerkfehlers fehlschlagen oder aber weil der Server nicht ausgeführt wird. Anstatt die standardmäßig festgelegten 20 Sekunden auf die Verbindung zu warten, können Sie festlegen, wie lange gewartet werden soll, bis ein Fehler erzeugt wird. Die Anmeldung beim Server wird implizit als Teil einer Reihe von verschiedenen Ereignissen ausgeführt, wie etwa beim Ausführen einer Abfrage einer externen Serverdatenbank.

