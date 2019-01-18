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
# <a name="configuring-virtual-servers-on-iis"></a><span data-ttu-id="ae36a-102">Konfigurieren von virtuellen Servern auf IIS</span><span class="sxs-lookup"><span data-stu-id="ae36a-102">Configuring virtual servers on IIS</span></span>

<span data-ttu-id="ae36a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae36a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ae36a-104">Beim Erstellen virtueller Server in Internetinformationsdienste (IIS) 4.0 müssen Sie zusätzlich die folgenden beiden Schritte ausführen, damit die virtuellen Server für eine Verwendung mit RDS konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="ae36a-104">When creating virtual servers in Internet Information Services 4.0, the following two extra steps are needed in order to configure the virtual server to work with RDS:</span></span>

1.  <span data-ttu-id="ae36a-105">Aktivieren Sie beim Einrichten des Servers Ausführen unter Folgendes zulassen.</span><span class="sxs-lookup"><span data-stu-id="ae36a-105">When setting up the server, check "Allow Execute Access."</span></span>

2.  <span data-ttu-id="ae36a-106">Verschieben Sie msadcs.dll nach *Vroot*\\Msadc, wobei *Vroot* das Stammverzeichnis des virtuellen Servers ist.</span><span class="sxs-lookup"><span data-stu-id="ae36a-106">Move msadcs.dll to *vroot*\\msadc, where *vroot* is the home directory of your virtual server.</span></span>

