---
title: Übersicht über den MAPI-Transportanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 20b03f7c52ec86d1fb554bf69c53947c3dda4f36
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404575"
---
# <a name="mapi-transport-provider-overview"></a><span data-ttu-id="6e646-103">Übersicht über den MAPI-Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="6e646-103">MAPI Transport Provider Overview</span></span>

  
  
<span data-ttu-id="6e646-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e646-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e646-105">Transportanbieter verarbeiten nachrichtenübermittlung und -empfang und implementieren bei Bedarf Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="6e646-105">Transport providers handle message transmission and reception and implement security, if necessary.</span></span> <span data-ttu-id="6e646-106">Außerdem übernehmen sie alle erforderlichen Vor- und Nachverarbeitungsaufgaben.</span><span class="sxs-lookup"><span data-stu-id="6e646-106">They also take care of any necessary preprocessing and postprocessing tasks.</span></span> <span data-ttu-id="6e646-107">Es gibt in der Regel einen Transportanbieter für jedes aktive Messagingsystem.</span><span class="sxs-lookup"><span data-stu-id="6e646-107">There is typically one transport provider for every active messaging system.</span></span>
  
<span data-ttu-id="6e646-108">Clientanwendungen kommunizieren mit dem Transportanbieter über einen Nachrichtenspeicheranbieter.</span><span class="sxs-lookup"><span data-stu-id="6e646-108">Client applications communicate with the transport provider through a message store provider.</span></span> 
  
<span data-ttu-id="6e646-109">Transportanbieter registrieren sich bei MAPI, um einen oder mehrere bestimmte Typen von Empfängereinträgen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="6e646-109">Transport providers register with MAPI to handle one or more particular types of recipient entries.</span></span> <span data-ttu-id="6e646-110">Wenn eine Nachricht gesendet werden kann, muss MAPI bestimmen, welcher Transportanbieter die Übertragung verarbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="6e646-110">When a message is ready to be sent, MAPI must determine which transport provider should handle the transmission.</span></span> <span data-ttu-id="6e646-111">Je nach Empfängertyp kann MAPI sogar mehrere Transportanbieter aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6e646-111">Depending on the type of recipient, MAPI can even call upon more than one transport provider.</span></span> <span data-ttu-id="6e646-112">Wenn ein nicht verfügbarer Transportanbieter der einzige ist, der den Empfänger verarbeiten kann, wird die Nachrichtenübertragung verschoben, bis eine Verbindung mit diesem Anbieter wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6e646-112">If an unavailable transport provider is the only one that can handle the recipient, the message transmission will be postponed until a connection with that provider can be reestablished.</span></span>
  
<span data-ttu-id="6e646-113">Einige Messagingsysteme sind sichere Systeme. Alle potenziellen Benutzer müssen einen Satz gültiger Anmeldeinformationen eingeben, bevor der Zugriff zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="6e646-113">Some messaging systems are secure systems; all potential users are required to enter a set of valid credentials before access is permitted.</span></span> <span data-ttu-id="6e646-114">MAPI verhindert nicht autorisierten Zugriff auf solche sicheren Messagingsysteme, indem der Transportanbieter anmeldeinformationen zum Zeitpunkt der Anmeldung überprüft.</span><span class="sxs-lookup"><span data-stu-id="6e646-114">MAPI prevents unauthorized access to such secure messaging systems by having the transport provider validate credentials at logon time.</span></span> 
  

