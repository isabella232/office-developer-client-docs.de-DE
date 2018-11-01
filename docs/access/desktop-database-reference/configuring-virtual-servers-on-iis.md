---
title: Konfigurieren virtueller Server in IIS
TOCTitle: Configuring Virtual Servers on IIS
ms:assetid: 0a8057a2-c90b-d0b5-21c8-5343e80708ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248837(v=office.15)
ms:contentKeyID: 48543154
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7408e2dc10a5e47b298b77a9244477b16bca3ff1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879242"
---
# <a name="configuring-virtual-servers-on-iis"></a>Konfigurieren virtueller Server in IIS


**Betrifft**: Access 2013, Office 2013

Beim Erstellen virtueller Server in Internetinformationsdienste (IIS) 4.0 müssen Sie zusätzlich die folgenden beiden Schritte ausführen, damit die virtuellen Server für eine Verwendung mit RDS konfiguriert werden können.

1.  Aktivieren Sie beim Einrichten des Servers Ausführen unter Folgendes zulassen.

2.  Verschieben Sie msadcs.dll nach *Vroot*\\Msadc, wobei *Vroot* das Stammverzeichnis des virtuellen Servers ist.

