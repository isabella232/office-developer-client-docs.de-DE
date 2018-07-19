---
title: Staren einer MAPI-Sitzung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d683d5fc959b219569417c74494cb47d7c2c059e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795623"
---
# <a name="starting-a-mapi-session"></a><span data-ttu-id="b85db-103">Staren einer MAPI-Sitzung</span><span class="sxs-lookup"><span data-stu-id="b85db-103">Starting a MAPI Session</span></span>

  
  
<span data-ttu-id="b85db-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b85db-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b85db-105">Es ist, zwar eine große Menge von Arbeit während der Sitzung starten sind die erforderlichen Aufgaben sehr gering.</span><span class="sxs-lookup"><span data-stu-id="b85db-105">Although there is a significant amount of work performed during session start up, the required tasks are minimal.</span></span> <span data-ttu-id="b85db-106">Viele dieser Aufgaben erfolgt in der MAPI Verarbeitung der Aufrufe der ["MAPIInitialize"](mapiinitialize.md) und [MAPILogonEx](mapilogonex.md) .</span><span class="sxs-lookup"><span data-stu-id="b85db-106">Much of this work is done in the MAPI processing of the [MAPIInitialize](mapiinitialize.md) and [MAPILogonEx](mapilogonex.md) calls.</span></span> <span data-ttu-id="b85db-107">Beide Funktionen akzeptieren Flags als Eingabeparameter für Aspekte der Sitzung wie Benachrichtigung Behandlung und die Benutzeroberfläche steuern.</span><span class="sxs-lookup"><span data-stu-id="b85db-107">Both of these functions accept flags as input parameters for controlling aspects of the session such as notification handling and the user interface.</span></span> <span data-ttu-id="b85db-108">Es ist wichtig zu verstehen, folgen die Festlegung jedes dieser Flags beim Aufrufen von **"MAPIInitialize"** zum Initialisieren der MAPI-Bibliotheken und **MAPILogonEx** zur Anmeldung bei der MAPI-Subsystems.</span><span class="sxs-lookup"><span data-stu-id="b85db-108">It is important to understand the consequences of setting each of these flags when calling **MAPIInitialize** to initialize the MAPI libraries and **MAPILogonEx** to log on to the MAPI subsystem.</span></span> 
  
 <span data-ttu-id="b85db-109">**Zum Starten einer MAPI-Sitzung**</span><span class="sxs-lookup"><span data-stu-id="b85db-109">**To start a MAPI session**</span></span>
  
1. <span data-ttu-id="b85db-110">Rufen Sie **"MAPIInitialize"** , um den Standardsatz von MAPI-Bibliotheken zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="b85db-110">Call **MAPIInitialize** to initialize the standard set of MAPI libraries.</span></span> 
    
2. <span data-ttu-id="b85db-111">Wenn Sie die OLE-Bibliotheken verwenden müssen, rufen Sie die OLE-Funktion [OleInitialize](http://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b85db-111">If you need to use the OLE libraries, call the OLE function [OleInitialize](http://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).</span></span>
    
3. <span data-ttu-id="b85db-112">Wenn Sie die Dienstprogramm MAPI-Bibliothek verwenden müssen, rufen Sie [ScInitMapiUtil](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="b85db-112">If you need to use the MAPI utility library, call [ScInitMapiUtil](scinitmapiutil.md).</span></span>
    
4. <span data-ttu-id="b85db-113">Rufen Sie mit einem gültigen Profil zur Anmeldung bei der MAPI-Subsystems **MAPILogonEx** .</span><span class="sxs-lookup"><span data-stu-id="b85db-113">Call **MAPILogonEx** with a valid profile to log on to the MAPI subsystem.</span></span> <span data-ttu-id="b85db-114">**MAPILogonEx** überprüft die Konfiguration der einzelnen-Dienstanbieter in der Nachrichtendienste im Profil enthalten zusätzliche Informationen der Benutzer aufgefordert wird, bei Bedarf und mögliche.</span><span class="sxs-lookup"><span data-stu-id="b85db-114">**MAPILogonEx** verifies the configuration of each of the service providers in the message services included in the profile, prompting the user for additional information if necessary and possible.</span></span> <span data-ttu-id="b85db-115">Wenn **MAPILogonEx** abgeschlossen ist, sind die konfigurierten-Dienstanbieter für den Dienst bereit.</span><span class="sxs-lookup"><span data-stu-id="b85db-115">When **MAPILogonEx** completes, the configured service providers are ready for service.</span></span> 
    
## <a name="in-this-section"></a><span data-ttu-id="b85db-116">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="b85db-116">In this section</span></span>

[<span data-ttu-id="b85db-117">Initialisieren von MAPI</span><span class="sxs-lookup"><span data-stu-id="b85db-117">Initializing MAPI</span></span>](initializing-mapi.md)
  
> <span data-ttu-id="b85db-118">Beschreibt, wie MAPI für eine Sitzung nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b85db-118">Describes how to initialize MAPI for a session.</span></span>
    
[<span data-ttu-id="b85db-119">Initialisieren von OLE für MAPI</span><span class="sxs-lookup"><span data-stu-id="b85db-119">Initializing OLE for MAPI</span></span>](initializing-ole-for-mapi.md)
  
> <span data-ttu-id="b85db-120">Beschreibt die Anrufe tätigen OLE für die Verwendung mit MAPI nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b85db-120">Describes the calls to make to initialize OLE for use with MAPI.</span></span>
    
[<span data-ttu-id="b85db-121">Initialisieren der MAPI-Dienstprogramme</span><span class="sxs-lookup"><span data-stu-id="b85db-121">Initializing the MAPI Utilities</span></span>](initializing-the-mapi-utilities.md)
  
> <span data-ttu-id="b85db-122">Beschreibt, wie MAPI-Dienstprogramme nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b85db-122">Describes how to initialize MAPI utilities.</span></span>
    
[<span data-ttu-id="b85db-123">Anmelden bei MAPI</span><span class="sxs-lookup"><span data-stu-id="b85db-123">Logging on to MAPI</span></span>](logging-on-to-mapi.md)
  
> <span data-ttu-id="b85db-124">Beschreibt, wie Clientanwendungen mit dem MAPI-Sub System anmelden.</span><span class="sxs-lookup"><span data-stu-id="b85db-124">Describes how client applications log on to the MAPI sub system.</span></span>
    

