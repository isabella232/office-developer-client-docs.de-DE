---
title: Konfigurieren virtueller Server in IIS
TOCTitle: Configuring Virtual Servers on IIS
ms:assetid: 0a8057a2-c90b-d0b5-21c8-5343e80708ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248837(v=office.15)
ms:contentKeyID: 48543154
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1212a5c7e0761cf9c52a21b5abd67b7dd9841aa0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473052"
---
# <a name="configuring-virtual-servers-on-iis"></a><span data-ttu-id="c77de-102">Konfigurieren virtueller Server in IIS</span><span class="sxs-lookup"><span data-stu-id="c77de-102">Configuring Virtual Servers on IIS</span></span>


<span data-ttu-id="c77de-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c77de-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c77de-104">Beim Erstellen virtueller Server in Internetinformationsdienste (IIS) 4.0 müssen Sie zusätzlich die folgenden beiden Schritte ausführen, damit die virtuellen Server für eine Verwendung mit RDS konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="c77de-104">When creating virtual servers in Internet Information Services 4.0, the following two extra steps are needed in order to configure the virtual server to work with RDS:</span></span>

1.  <span data-ttu-id="c77de-105">Aktivieren Sie beim Einrichten des Servers Ausführen unter Folgendes zulassen.</span><span class="sxs-lookup"><span data-stu-id="c77de-105">When setting up the server, check "Allow Execute Access."</span></span>

2.  <span data-ttu-id="c77de-106">Verschieben Sie msadcs.dll nach *Vroot*\\Msadc, wobei *Vroot* das Stammverzeichnis des virtuellen Servers ist.</span><span class="sxs-lookup"><span data-stu-id="c77de-106">Move msadcs.dll to *vroot*\\msadc, where *vroot* is the home directory of your virtual server.</span></span>

