---
title: DBEngine.LoginTimeout-Eigenschaft (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 81d14153-79c5-7860-b6a8-4079d2d7acf7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196648(v=office.15)
ms:contentKeyID: 48545964
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052923
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: e3ff893a16e650fe7eb49b647ae8d67374375a0d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701928"
---
# <a name="dbenginelogintimeout-property-dao"></a>DBEngine.LoginTimeout-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Legt fest, wie viele Sekunden gewartet wird, bis ein Fehler auftritt, wenn versucht wird, sich bei einer ODBC-Datenbank anzumelden, oder gibt die betreffende Anzahl von Sekunden zurück.

## <a name="syntax"></a>Syntax

*Ausdruck* . LoginTimeout

*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die Standardeinstellung der LoginTimeout-Eigenschaft beträgt 20 Sekunden. Wenn die LoginTimeout-Eigenschaft auf 0 gesetzt ist, tritt kein Timeout ein.

Wenn Sie versuchen, sich bei einer ODBC-Datenbank anzumelden, wie etwa bei Microsoft SQL Server, kann die Verbindung aufgrund eines Netzwerkfehlers fehlschlagen oder aber weil der Server nicht ausgeführt wird. Anstatt die standardmäßig festgelegten 20 Sekunden auf die Verbindung zu warten, können Sie festlegen, wie lange gewartet werden soll, bis ein Fehler erzeugt wird. Die Anmeldung beim Server wird implizit als Teil einer Reihe von verschiedenen Ereignissen ausgeführt, wie etwa beim Ausführen einer Abfrage einer externen Serverdatenbank.

