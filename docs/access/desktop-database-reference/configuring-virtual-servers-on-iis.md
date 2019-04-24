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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295975"
---
# <a name="configuring-virtual-servers-on-iis"></a><span data-ttu-id="6cd0b-102">Konfigurieren von virtuellen Servern auf IIS</span><span class="sxs-lookup"><span data-stu-id="6cd0b-102">Configuring virtual servers on IIS</span></span>

<span data-ttu-id="6cd0b-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6cd0b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6cd0b-104">Beim Erstellen virtueller Server in Internetinformationsdienste (IIS) 4.0 müssen Sie zusätzlich die folgenden beiden Schritte ausführen, damit die virtuellen Server für eine Verwendung mit RDS konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="6cd0b-104">When creating virtual servers in Internet Information Services 4.0, the following two extra steps are needed in order to configure the virtual server to work with RDS:</span></span>

1.  <span data-ttu-id="6cd0b-105">When setting up the server, check "Allow Execute Access."</span><span class="sxs-lookup"><span data-stu-id="6cd0b-105">When setting up the server, check "Allow Execute Access."</span></span>

2.  <span data-ttu-id="6cd0b-106">Verschieben Sie Msadcs. dll in *vroot*\\MSADC, wobei *vroot* das Basisverzeichnis des virtuellen Servers ist.</span><span class="sxs-lookup"><span data-stu-id="6cd0b-106">Move msadcs.dll to *vroot*\\msadc, where *vroot* is the home directory of your virtual server.</span></span>

