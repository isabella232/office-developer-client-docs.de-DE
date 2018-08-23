---
title: Implementieren von Sicherheitsmaßnahmen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62db34a0-887c-4607-94ad-d8cae68b35c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c2926e7c94178d5a3135f34e2ab3b3ae11d145dd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568483"
---
# <a name="implementing-security"></a><span data-ttu-id="35ba7-103">Implementieren von Sicherheitsmaßnahmen</span><span class="sxs-lookup"><span data-stu-id="35ba7-103">Implementing Security</span></span>

  
  
<span data-ttu-id="35ba7-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35ba7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35ba7-105">Wenn das messaging-System erforderlich sind, ist der Adressbuchhierarchie verantwortlich für die Implementierung der Sicherheit für den Zugriff auf die messaging-System einer angemessene Lautstärke.</span><span class="sxs-lookup"><span data-stu-id="35ba7-105">If the messaging system requires it, the transport provider is responsible for implementing an appropriate level of security for access to the messaging system.</span></span> <span data-ttu-id="35ba7-106">Jedes ein- oder ausgehende Nachricht über einen Transportanbieter durch die MAPI-Warteschlange wird im Zusammenhang mit einer Sitzung Anbieter behandelt.</span><span class="sxs-lookup"><span data-stu-id="35ba7-106">Each incoming or outgoing message sent through a transport provider by the MAPI spooler is handled in the context of a provider logon session.</span></span> <span data-ttu-id="35ba7-107">Der Adressbuchhierarchie kann ein Anmeldedialogfeld für den Benutzer angezeigt, die für die Anmeldeinformationen des Benutzers aufgefordert werden, bevor er eine solche Verbindung.</span><span class="sxs-lookup"><span data-stu-id="35ba7-107">The transport provider can display a logon dialog box to the user that prompts for a user's credentials before establishing such a connection.</span></span> <span data-ttu-id="35ba7-108">Alternativ kann der Adressbuchhierarchie zuvor eingegebenen Anmeldeinformationen des Benutzers im Bereich diese Eigenschaft in einem Profilabschnitt speichern und verwenden sie für den Zugriff ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="35ba7-108">Alternatively, the transport provider can store the user's previously entered credentials in the secure property range within a profile section and use them for access without prompting.</span></span>
  
<span data-ttu-id="35ba7-109">Berücksichtigen Sie beim Implementieren von Ihrer Adressbuchhierarchie Sicherheit Folgendes:</span><span class="sxs-lookup"><span data-stu-id="35ba7-109">When implementing your transport provider's security, consider the following:</span></span>
  
- <span data-ttu-id="35ba7-110">Mit mehreren installierten Dienstanbieter können eine Vielzahl von Namen und Kennwörter, die einem Benutzer zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="35ba7-110">With multiple installed service providers, there can be a multitude of names and passwords associated with a user.</span></span>
    
- <span data-ttu-id="35ba7-111">MAPI ermöglicht mehrerer Sitzungen mit mehreren Identitäten.</span><span class="sxs-lookup"><span data-stu-id="35ba7-111">MAPI allows multiple sessions with multiple identities.</span></span> <span data-ttu-id="35ba7-112">Anbieter werden empfohlen, die Unterstützung mehrerer Sitzungen aber nicht dazu erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="35ba7-112">Providers are encouraged to support multiple sessions but are not required to do so.</span></span>
    
- <span data-ttu-id="35ba7-113">Jede Sitzung mit eines Transportdienstes ist MAPI einen getrennten Abschnitt im Profil des Benutzers zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="35ba7-113">Each session with a transport provider is associated by MAPI with a discrete section in the user's profile.</span></span> <span data-ttu-id="35ba7-114">Der Transportdienst kann die [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) -Methode verwenden, den Zugriff auf die in diesem Abschnitt, die verwendet werden kann, um alle Informationen im Zusammenhang mit dieser Sitzung, einschließlich der Anmeldeinformationen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="35ba7-114">The transport provider can use the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to gain access to this section, which can be used to store any information associated with this session, including credentials.</span></span> 
    
- <span data-ttu-id="35ba7-115">Mit mehreren Anbietern installierten Transport gilt es nicht unbedingt, dass der Benutzer nur eine einzelne e-Mail-Adresse verfügt.</span><span class="sxs-lookup"><span data-stu-id="35ba7-115">With multiple installed transport providers, it is not necessarily true that the user only has a single email address.</span></span> <span data-ttu-id="35ba7-116">Ein Benutzer kann eine separate e-Mail-Adresse für jeden Transportanbieter installierten haben oder eine andere Adresse für jede Sitzung auf einen einzigen Anbieter aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="35ba7-116">A user can have a separate email address for each installed transport provider or can have a different address for each session on a single provider.</span></span>
    
<span data-ttu-id="35ba7-117">Weitere Informationen zum Speichern von Anmeldeinformationen in Profil Abschnitten finden Sie unter [Message-Dienste und -Profilen](message-services-and-profiles.md) und [IProfSect: IMAPIProp](iprofsectimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="35ba7-117">For more information about storing credentials in profile sections, see [Message Services and Profiles](message-services-and-profiles.md) and [IProfSect : IMAPIProp](iprofsectimapiprop.md).</span></span>
  

