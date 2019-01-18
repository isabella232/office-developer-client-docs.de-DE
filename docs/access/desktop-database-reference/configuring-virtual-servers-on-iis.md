---
title: Konfigurieren von virtuellen Servern auf IIS
TOCTitle: Configuring virtual servers on IIS
ms:assetid: 0a8057a2-c90b-d0b5-21c8-5343e80708ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248837(v=office.15)
ms:contentKeyID: 48543154
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9c7f5782885aafd43e365ddc4f08dedd0975234
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719314"
---
# <a name="configuring-virtual-servers-on-iis"></a>Konfigurieren von virtuellen Servern auf IIS

**Betrifft**: Access 2013, Office 2013

Beim Erstellen virtueller Server in Internetinformationsdienste (IIS) 4.0 müssen Sie zusätzlich die folgenden beiden Schritte ausführen, damit die virtuellen Server für eine Verwendung mit RDS konfiguriert werden können.

1.  Aktivieren Sie beim Einrichten des Servers Ausführen unter Folgendes zulassen.

2.  Verschieben Sie msadcs.dll nach *Vroot*\\Msadc, wobei *Vroot* das Stammverzeichnis des virtuellen Servers ist.

