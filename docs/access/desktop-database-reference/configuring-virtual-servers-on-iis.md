---
title: Konfigurieren von virtuellen Servern auf IIS
TOCTitle: Configuring virtual servers on IIS
ms:assetid: 0a8057a2-c90b-d0b5-21c8-5343e80708ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248837(v=office.15)
ms:contentKeyID: 48543154
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: db240ef561de9ba653dbad3453a2ee4d894baa25
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602892"
---
# <a name="configuring-virtual-servers-on-iis"></a>Konfigurieren von virtuellen Servern auf IIS

**Gilt für**: Access 2013, Office 2013

Beim Erstellen virtueller Server in Internetinformationsdienste (IIS) 4.0 müssen Sie zusätzlich die folgenden beiden Schritte ausführen, damit die virtuellen Server für eine Verwendung mit RDS konfiguriert werden können.

1.  When setting up the server, check "Allow Execute Access."

2.  Verschieben Sie msadcs.dll nach *vroot* \\ msadc, wobei *vroot* das Startverzeichnis Des virtuellen Servers ist.

