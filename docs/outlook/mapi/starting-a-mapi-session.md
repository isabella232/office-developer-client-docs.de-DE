---
title: Starten einer MAPI-Sitzung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d88ce382b6a6b5f98ec5f88c4deb1565d3b60151
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336344"
---
# <a name="starting-a-mapi-session"></a><span data-ttu-id="b9832-103">Starten einer MAPI-Sitzung</span><span class="sxs-lookup"><span data-stu-id="b9832-103">Starting a MAPI Session</span></span>

  
  
<span data-ttu-id="b9832-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9832-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9832-105">Obwohl während des Starts der Sitzung eine beträchtliche Menge an Arbeit ausgeführt wird, sind die erforderlichen Aufgaben minimal.</span><span class="sxs-lookup"><span data-stu-id="b9832-105">Although there is a significant amount of work performed during session start up, the required tasks are minimal.</span></span> <span data-ttu-id="b9832-106">Ein Großteil dieser Arbeit wird in der MAPI-Verarbeitung der [MAPIInitialize](mapiinitialize.md) -und [MAPILogonEx](mapilogonex.md) -Aufrufe ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9832-106">Much of this work is done in the MAPI processing of the [MAPIInitialize](mapiinitialize.md) and [MAPILogonEx](mapilogonex.md) calls.</span></span> <span data-ttu-id="b9832-107">Beide Funktionen akzeptieren Flags als Eingabeparameter für die Steuerung von Aspekten der Sitzung wie Benachrichtigungs Verarbeitung und Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="b9832-107">Both of these functions accept flags as input parameters for controlling aspects of the session such as notification handling and the user interface.</span></span> <span data-ttu-id="b9832-108">Es ist wichtig zu verstehen, welche Konsequenzen es hat, wenn Sie **MAPIInitialize** aufrufen, um die MAPI-Bibliotheken und **MAPILogonEx** zum Anmelden beim MAPI-Subsystem zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="b9832-108">It is important to understand the consequences of setting each of these flags when calling **MAPIInitialize** to initialize the MAPI libraries and **MAPILogonEx** to log on to the MAPI subsystem.</span></span> 
  
 <span data-ttu-id="b9832-109">**So starten Sie eine MAPI-Sitzung**</span><span class="sxs-lookup"><span data-stu-id="b9832-109">**To start a MAPI session**</span></span>
  
1. <span data-ttu-id="b9832-110">Rufen Sie **MAPIInitialize** auf, um den Standardsatz von MAPI-Bibliotheken zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="b9832-110">Call **MAPIInitialize** to initialize the standard set of MAPI libraries.</span></span> 
    
2. <span data-ttu-id="b9832-111">Wenn Sie die OLE-Bibliotheken verwenden müssen, rufen Sie die OLE-Funktion [OleInitialize](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b9832-111">If you need to use the OLE libraries, call the OLE function [OleInitialize](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span></span>
    
3. <span data-ttu-id="b9832-112">Wenn Sie die MAPI-Hilfsprogramm-Bibliothek verwenden müssen, rufen Sie [ScInitMapiUtil](scinitmapiutil.md)auf.</span><span class="sxs-lookup"><span data-stu-id="b9832-112">If you need to use the MAPI utility library, call [ScInitMapiUtil](scinitmapiutil.md).</span></span>
    
4. <span data-ttu-id="b9832-113">Rufen Sie **MAPILogonEx** mit einem gültigen Profil auf, um sich beim MAPI-Subsystem anzumelden.</span><span class="sxs-lookup"><span data-stu-id="b9832-113">Call **MAPILogonEx** with a valid profile to log on to the MAPI subsystem.</span></span> <span data-ttu-id="b9832-114">**MAPILogonEx** überprüft die Konfiguration der einzelnen Dienstanbieter in den im Profil enthaltenen Nachrichtendiensten, woraufhin der Benutzer erforderlichenfalls zusätzliche Informationen dazu auffordert.</span><span class="sxs-lookup"><span data-stu-id="b9832-114">**MAPILogonEx** verifies the configuration of each of the service providers in the message services included in the profile, prompting the user for additional information if necessary and possible.</span></span> <span data-ttu-id="b9832-115">Wenn **MAPILogonEx** abgeschlossen ist, sind die konfigurierten Dienstanbieter bereit für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="b9832-115">When **MAPILogonEx** completes, the configured service providers are ready for service.</span></span> 
    
## <a name="in-this-section"></a><span data-ttu-id="b9832-116">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="b9832-116">In this section</span></span>

[<span data-ttu-id="b9832-117">Initialisieren von MAPI</span><span class="sxs-lookup"><span data-stu-id="b9832-117">Initializing MAPI</span></span>](initializing-mapi.md)
  
> <span data-ttu-id="b9832-118">Beschreibt, wie Sie MAPI für eine Sitzung initialisieren.</span><span class="sxs-lookup"><span data-stu-id="b9832-118">Describes how to initialize MAPI for a session.</span></span>
    
[<span data-ttu-id="b9832-119">Initialisieren von OLE für MAPI</span><span class="sxs-lookup"><span data-stu-id="b9832-119">Initializing OLE for MAPI</span></span>](initializing-ole-for-mapi.md)
  
> <span data-ttu-id="b9832-120">Beschreibt die Aufrufe zum Initialisieren von OLE zur Verwendung mit MAPI.</span><span class="sxs-lookup"><span data-stu-id="b9832-120">Describes the calls to make to initialize OLE for use with MAPI.</span></span>
    
[<span data-ttu-id="b9832-121">Initialisieren der MAPI-Dienstprogramme</span><span class="sxs-lookup"><span data-stu-id="b9832-121">Initializing the MAPI Utilities</span></span>](initializing-the-mapi-utilities.md)
  
> <span data-ttu-id="b9832-122">Beschreibt, wie MAPI-Dienstprogramme initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b9832-122">Describes how to initialize MAPI utilities.</span></span>
    
[<span data-ttu-id="b9832-123">Anmelden bei MAPI</span><span class="sxs-lookup"><span data-stu-id="b9832-123">Logging on to MAPI</span></span>](logging-on-to-mapi.md)
  
> <span data-ttu-id="b9832-124">Beschreibt, wie sich Clientanwendungen am MAPI-Subsystem anmelden.</span><span class="sxs-lookup"><span data-stu-id="b9832-124">Describes how client applications log on to the MAPI sub system.</span></span>
    

