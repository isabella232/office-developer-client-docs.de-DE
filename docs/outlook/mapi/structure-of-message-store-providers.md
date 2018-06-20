---
title: Struktur der Nachricht-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2f78428b8067b7937e9bd2ee36934cc29a16bfb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795670"
---
# <a name="structure-of-message-store-providers"></a><span data-ttu-id="ea780-103">Struktur der Nachricht-Anbieter</span><span class="sxs-lookup"><span data-stu-id="ea780-103">Structure of message store providers</span></span>
  
<span data-ttu-id="ea780-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ea780-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ea780-105">Anbieter eine Nachricht bei der Ausführung im Arbeitsspeicher, ist eine [IMSProvider: IUnknown](imsprovideriunknown.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ea780-105">A message store provider, when it is running in memory, is an [IMSProvider : IUnknown](imsprovideriunknown.md) interface.</span></span> <span data-ttu-id="ea780-106">Die **IMSProvider** -Schnittstelle ermöglicht Client-Anwendungen und die MAPI-Warteschlange an und von der Nachrichtenspeicher anmelden.</span><span class="sxs-lookup"><span data-stu-id="ea780-106">The **IMSProvider** interface allows client applications and the MAPI spooler to log on to and off of the message store.</span></span> <span data-ttu-id="ea780-107">Die, die Clientanwendungen und die MAPI-Warteschlange verwenden, Zugriff auf Ordner und Nachrichten im Nachrichtenspeicher sind [IMSLogon](imslogoniunknown.md) und [IMsgStore](imsgstoreimapiprop.md) Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="ea780-107">The interfaces that client applications and the MAPI spooler use to access folders and messages in the message store are [IMSLogon](imslogoniunknown.md) and [IMsgStore](imsgstoreimapiprop.md) interfaces.</span></span> <span data-ttu-id="ea780-108">Diese Schnittstellen werden normalerweise erstellt, wenn der Nachrichtenspeicher zuerst angemeldet ist, obwohl der Einstiegspunkt [MSProviderInit](msproviderinit.md) der Nachricht speichern DLL konnte auch erstellen sie.</span><span class="sxs-lookup"><span data-stu-id="ea780-108">These interfaces are typically created when the message store is first logged on to, although the [MSProviderInit](msproviderinit.md) entry point of the message store DLL could also create them.</span></span> 
  
<span data-ttu-id="ea780-109">Da die **IMSLogon** und **IMsgStore** Schnittstellen einige Methoden gemeinsam nutzen, kann es einfacher sein ein Klassenobjekt erstellen, die beide Schnittstellen erbt.</span><span class="sxs-lookup"><span data-stu-id="ea780-109">Because the **IMSLogon** and **IMsgStore** interfaces share some methods, it may be easier to create one class object that inherits from both of these interfaces.</span></span> <span data-ttu-id="ea780-110">Sie können diese Schnittstellen in separaten Objekten implementieren, und Schreiben Hilfsfunktionen interne zur DLL, mit die die freigegebenen Methoden implementiert, die dann von den Methoden in den Schnittstellen **IMSLogon** und **IMsgStore** aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="ea780-110">You can also implement these interfaces in separate objects, and write helper functions internal to your DLL that implement the shared methods that can then be called from the methods in the **IMSLogon** and **IMsgStore** interfaces.</span></span> 
  
<span data-ttu-id="ea780-111">Die folgende Abbildung zeigt einen allgemeinen Überblick über die Objekthierarchie innerhalb eines Nachrichtenspeichers ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea780-111">The following illustration shows a high-level outline of the object hierarchy within a running message store.</span></span>
  
<span data-ttu-id="ea780-112">**Objekthierarchie des Nachrichtenspeichers**</span><span class="sxs-lookup"><span data-stu-id="ea780-112">**Message store object hierarchy**</span></span>
  
<span data-ttu-id="ea780-113">![Objekthierarchie des Nachrichtenspeichers] (media/storeobj.gif "Objekthierarchie des Nachrichtenspeichers")</span><span class="sxs-lookup"><span data-stu-id="ea780-113">![Message store object hierarchy](media/storeobj.gif "Message store object hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ea780-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea780-114">See also</span></span>

- [<span data-ttu-id="ea780-115">Entwickeln eines Providers MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="ea780-115">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

