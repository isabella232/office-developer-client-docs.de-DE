---
title: Übersicht über die MAPI-Transport-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 11cd1040bb228d789248a89184572b87cd1688ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793105"
---
# <a name="mapi-transport-provider-overview"></a><span data-ttu-id="69a25-103">Übersicht über die MAPI-Transport-Anbieter</span><span class="sxs-lookup"><span data-stu-id="69a25-103">MAPI Transport Provider Overview</span></span>

  
  
<span data-ttu-id="69a25-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="69a25-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="69a25-105">Transportanbieter die Nachrichtenübermittlung und Empfang verarbeiten und Implementieren von Sicherheit, falls dies erforderlich.</span><span class="sxs-lookup"><span data-stu-id="69a25-105">Transport providers handle message transmission and reception and implement security, if necessary.</span></span> <span data-ttu-id="69a25-106">Sie auch alle erforderlichen vorverarbeitung und übernehmen postprocessing Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="69a25-106">They also take care of any necessary preprocessing and postprocessing tasks.</span></span> <span data-ttu-id="69a25-107">In der Regel eine Adressbuchhierarchie für jede active messaging-System ist vorhanden.</span><span class="sxs-lookup"><span data-stu-id="69a25-107">There is typically one transport provider for every active messaging system.</span></span>
  
<span data-ttu-id="69a25-108">Clientanwendungen kommunizieren mit der Adressbuchhierarchie über einen Anbieter für die Nachricht anmelden.</span><span class="sxs-lookup"><span data-stu-id="69a25-108">Client applications communicate with the transport provider through a message store provider.</span></span> 
  
<span data-ttu-id="69a25-109">Transportanbieter registrieren MAPI, um eine oder mehrere bestimmte Arten von empfangenen Einträge zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="69a25-109">Transport providers register with MAPI to handle one or more particular types of recipient entries.</span></span> <span data-ttu-id="69a25-110">Wenn eine Nachricht gesendet werden kann, muss MAPI ermitteln, welche Adressbuchhierarchie die Übertragung behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="69a25-110">When a message is ready to be sent, MAPI must determine which transport provider should handle the transmission.</span></span> <span data-ttu-id="69a25-111">MAPI kann für mehrere Adressbuchhierarchie je nach Typ des Empfängers sogar hinzuziehen.</span><span class="sxs-lookup"><span data-stu-id="69a25-111">Depending on the type of recipient, MAPI can even call upon more than one transport provider.</span></span> <span data-ttu-id="69a25-112">Ist eine nicht verfügbare Adressbuchhierarchie die einzige, die den Empfänger verarbeitet werden können, wird der Nachrichtenübermittlung verschoben werden, bis eine Verbindung mit diesem Anbieter wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="69a25-112">If an unavailable transport provider is the only one that can handle the recipient, the message transmission will be postponed until a connection with that provider can be reestablished.</span></span>
  
<span data-ttu-id="69a25-113">Einige Messagingsysteme sind sichere Systeme. Alle potenzielle Benutzern sind erforderlich, um einen Satz von gültige Anmeldeinformationen eingeben, vor dem Zugriff zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="69a25-113">Some messaging systems are secure systems; all potential users are required to enter a set of valid credentials before access is permitted.</span></span> <span data-ttu-id="69a25-114">MAPI verhindert nicht autorisierten Zugriff auf solchen secure messaging-Systemen, dass der Adressbuchhierarchie Anmeldeinformationen bei der Anmeldung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="69a25-114">MAPI prevents unauthorized access to such secure messaging systems by having the transport provider validate credentials at logon time.</span></span> 
  
