---
title: Speicherszenario für XML-Recordset
TOCTitle: XML Recordset Persistence Scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2bbb8a3aa50027be7ce025a04d5987a45fee888f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475503"
---
# <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="73c57-102">Speicherszenario für XML-Recordset</span><span class="sxs-lookup"><span data-stu-id="73c57-102">XML Recordset Persistence Scenario</span></span>


<span data-ttu-id="73c57-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="73c57-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="73c57-104">Speicherszenario für XML-Recordset</span><span class="sxs-lookup"><span data-stu-id="73c57-104">XML Recordset Persistence Scenario</span></span>

<span data-ttu-id="73c57-105">In diesem Szenario erstellen Sie eine ASP-Anwendung (Active Server Pages), die den Inhalt eines **Recordset** -Objekts direkt in das **ASP-Response** -Objekt speichert.</span><span class="sxs-lookup"><span data-stu-id="73c57-105">In this scenario, you will create an Active Server Pages (ASP) application that saves the contents of a **Recordset** object directly to the ASP **Response** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="73c57-106">[!HINWEIS] Für dieses Szenario muss Internetinformationsdienste (IIS) 5.0 oder höher installiert sein.</span><span class="sxs-lookup"><span data-stu-id="73c57-106">This scenario requires that your server have Internet Information Server 5.0 (IIS) or later installed.</span></span></P>



<span data-ttu-id="73c57-107">Das zurückgegebene **Recordset** -Objekt wird unter Verwendung eines [RDS.DataControl](datacontrol-object-rds.md)-Objekts in Internet Explorer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="73c57-107">The returned **Recordset** is displayed in Internet Explorer using an [RDS.DataControl](datacontrol-object-rds.md).</span></span>

<span data-ttu-id="73c57-108">Die folgenden Schritte sind für dieses Szenario erforderlich:</span><span class="sxs-lookup"><span data-stu-id="73c57-108">The following steps are necessary to create this scenario:</span></span>

1.  <span data-ttu-id="73c57-109">Einrichten der Anwendung</span><span class="sxs-lookup"><span data-stu-id="73c57-109">Set up the application.</span></span>

2.  <span data-ttu-id="73c57-110">Abrufen der Daten</span><span class="sxs-lookup"><span data-stu-id="73c57-110">Get the data.</span></span>

3.  <span data-ttu-id="73c57-111">Senden der Daten</span><span class="sxs-lookup"><span data-stu-id="73c57-111">Send the data.</span></span>

4.  <span data-ttu-id="73c57-112">Empfangen und Anzeigen der Daten</span><span class="sxs-lookup"><span data-stu-id="73c57-112">Receive and display the data.</span></span>

<span data-ttu-id="73c57-113">**Weiter mit**[Schritt 1: Einrichten der Anwendung](step-1-set-up-the-application.md)</span><span class="sxs-lookup"><span data-stu-id="73c57-113">**Next**[Step 1: Set Up the Application](step-1-set-up-the-application.md)</span></span>

