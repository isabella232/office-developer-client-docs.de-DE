---
title: MAPI-Sitzungs Verarbeitung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 98c4bd0dba630db32fdb2309be3d29ebc13b1131
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422061"
---
# <a name="mapi-session-handling"></a><span data-ttu-id="d2dbf-103">MAPI-Sitzungs Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="d2dbf-103">MAPI Session Handling</span></span>

  
  
<span data-ttu-id="d2dbf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2dbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2dbf-105">Bevor Sie mit Dienstanbietern und einem zugrunde liegenden Messagingsystem kommunizieren können, müssen Sie eine Sitzung erstellen.</span><span class="sxs-lookup"><span data-stu-id="d2dbf-105">Before you can communicate with service providers and an underlying messaging system, you must establish a session.</span></span> <span data-ttu-id="d2dbf-106">Eine MAPI-Sitzung ist ein Link von einem Client zu anderen MAPI-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="d2dbf-106">A MAPI session is a link from a client to other MAPI components.</span></span> <span data-ttu-id="d2dbf-107">Als Ergebnis des erfolgreichen Startens einer Sitzung gibt MAPI an Clients einen Zeiger auf ein Session-Objekt zurück, ein Objekt, das die **IMAPISession** -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="d2dbf-107">As the result of successfully starting a session, MAPI returns to clients a pointer to a session object — an object that implements the **IMAPISession** interface.</span></span> <span data-ttu-id="d2dbf-108">Weitere Informationen finden Sie unter [IMAPISession: IUnknown](imapisessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="d2dbf-108">For more information, see [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span> <span data-ttu-id="d2dbf-109">Sie können die Methoden der **IMAPISession** -Schnittstelle verwenden, um auf die Objekte von Adressbuch-und Nachrichtenspeicher Anbietern zuzugreifen, auf mehrere Tabellen zuzugreifen, Formulare anzuzeigen, Transportanbieter Eigenschaften festzulegen und die Verwaltung von Profil-und Nachrichtendiensten durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="d2dbf-109">You can use the methods of the **IMAPISession** interface to access the objects of address book and message store providers, access several tables, display forms, set transport provider properties, and perform profile and message service administration.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="d2dbf-110">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="d2dbf-110">In this section</span></span>

[<span data-ttu-id="d2dbf-111">Starten einer MAPI-Sitzung</span><span class="sxs-lookup"><span data-stu-id="d2dbf-111">Starting a MAPI Session</span></span>](starting-a-mapi-session.md)
  
> <span data-ttu-id="d2dbf-112">Beschreibt das Starten einer MAPI-Sitzung und enthält Links zu Themen mit detaillierteren Informationen.</span><span class="sxs-lookup"><span data-stu-id="d2dbf-112">Describes how to start a MAPI session and includes links to topics with more detailed information.</span></span>
    
[<span data-ttu-id="d2dbf-113">Beenden einer MAPI-Sitzung</span><span class="sxs-lookup"><span data-stu-id="d2dbf-113">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)
  
> <span data-ttu-id="d2dbf-114">Beschreibt das Beenden einer MAPI-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="d2dbf-114">Describes how to end a MAPI session.</span></span>
    
[<span data-ttu-id="d2dbf-115">Zugreifen auf Objekte mithilfe der Sitzung</span><span class="sxs-lookup"><span data-stu-id="d2dbf-115">Accessing Objects by Using the Session</span></span>](accessing-objects-by-using-the-session.md)
  
> <span data-ttu-id="d2dbf-116">Beschreibt die Verwendung eines Sitzungs Zeigers für den Zugriff auf Sitzungsobjekte.</span><span class="sxs-lookup"><span data-stu-id="d2dbf-116">Describes how to use a session pointer to access session objects.</span></span>
    
[<span data-ttu-id="d2dbf-117">Abrufen der primären und Anbieter Identität</span><span class="sxs-lookup"><span data-stu-id="d2dbf-117">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
> <span data-ttu-id="d2dbf-118">Beschreibt die Eigenschaften, die zum Abrufen der primären und Anbieter Identität verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d2dbf-118">Describes the properties used to retrieve primary and provider identity.</span></span>
    
[<span data-ttu-id="d2dbf-119">Statustabelle und Statusobjekte</span><span class="sxs-lookup"><span data-stu-id="d2dbf-119">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)
  
> <span data-ttu-id="d2dbf-120">Beschreibt, wie auf Informationen aus der Statustabelle zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="d2dbf-120">Describes how to access information from the status table.</span></span>
    

