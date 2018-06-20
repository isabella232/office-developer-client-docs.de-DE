---
title: Zum Beispiel Offline State-Add-in
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a6bdf408-114a-2203-189f-101251a65a8c
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9a4dbe6757ae7ce5eccee3c3a366660db412cfe6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791238"
---
# <a name="about-the-sample-offline-state-add-in"></a><span data-ttu-id="fd4a1-103">Zum Beispiel Offline State-Add-in</span><span class="sxs-lookup"><span data-stu-id="fd4a1-103">About the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="fd4a1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fd4a1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fd4a1-105">Die Offline Zustand-API unterstützt, der angibt, Änderungen in Verbindungsstatus in Outlook des Benutzers Rückrufe – beispielsweise verhindern in Outlook online zu offline.</span><span class="sxs-lookup"><span data-stu-id="fd4a1-105">The Offline State API supports callbacks indicating changes in a user's connection state in Outlook—for example, from being online in Outlook to being offline.</span></span> <span data-ttu-id="fd4a1-106">Das Beispiel Offline Zustand-Add-in ist eines COM-add-Ins in C++, der zum Empfangen von Benachrichtigungen der Verbindung Status ändert sich wie und so ändern Sie den aktuellen Status verwenden Zustand-API geschrieben.</span><span class="sxs-lookup"><span data-stu-id="fd4a1-106">The Sample Offline State Add-in is a COM add-in written in C++ that demonstrates how to receive notifications of connection state changes and how to modify the current state using the Offline State API.</span></span> <span data-ttu-id="fd4a1-107">Weitere Informationen zur Status-API finden Sie unter [Über die Offline Zustand-API](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="fd4a1-107">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="fd4a1-108">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="fd4a1-108">In this section</span></span>

- [<span data-ttu-id="fd4a1-109">Installieren das Beispiel Offline State-Add-in</span><span class="sxs-lookup"><span data-stu-id="fd4a1-109">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
    
- <span data-ttu-id="fd4a1-110">Erläutert das Herunterladen und Offline-Status Beispiel-Add-in installieren.</span><span class="sxs-lookup"><span data-stu-id="fd4a1-110">Explains how to download and install the Sample Offline State Add-in.</span></span>
    
- [<span data-ttu-id="fd4a1-111">Einrichten von einem Offline State Add-in</span><span class="sxs-lookup"><span data-stu-id="fd4a1-111">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
    
- <span data-ttu-id="fd4a1-112">Beschreibt, wie Verbindung, Initialisierung und Setup-Funktionen zu implementieren, um ein Add-in-offline-Status zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fd4a1-112">Describes how to implement connection, initialization, and setup functions in order to use an offline state add-in.</span></span>
    
- [<span data-ttu-id="fd4a1-113">Überwachung Verbindungsstatus ändert mit einer Offline State-Add-in</span><span class="sxs-lookup"><span data-stu-id="fd4a1-113">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
    
- <span data-ttu-id="fd4a1-114">Beschreibt, wie die **[HrOpenOfflineObj](hropenofflineobj.md)** -Funktion zu verwenden, um ein offline-Objekt zum Überwachen und Ändern des Verbindungsstatus abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fd4a1-114">Describes how to use the **[HrOpenOfflineObj](hropenofflineobj.md)** function to obtain an offline object to monitor and change the connection state.</span></span> 
    
- [<span data-ttu-id="fd4a1-115">Trennen der Verbindung ein Offline State-Add-in</span><span class="sxs-lookup"><span data-stu-id="fd4a1-115">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)
    
- <span data-ttu-id="fd4a1-116">Beschreibt, wie ordnungsgemäß beendet und Bereinigen von offline-Status-Add-in, wenn das Add-in getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="fd4a1-116">Describes how to properly terminate and clean up an offline state add-in when the add-in is disconnected.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fd4a1-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd4a1-117">See also</span></span>



[<span data-ttu-id="fd4a1-118">Über die Offline State-API</span><span class="sxs-lookup"><span data-stu-id="fd4a1-118">About the Offline State API</span></span>](about-the-offline-state-api.md)

