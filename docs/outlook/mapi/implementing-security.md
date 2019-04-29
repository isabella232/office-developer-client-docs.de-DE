---
title: Implementieren von Sicherheit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62db34a0-887c-4607-94ad-d8cae68b35c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c430160ee508a86f36d840c7916c0516cfc10fbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417287"
---
# <a name="implementing-security"></a><span data-ttu-id="7c4ec-103">Implementieren von Sicherheit</span><span class="sxs-lookup"><span data-stu-id="7c4ec-103">Implementing Security</span></span>

  
  
<span data-ttu-id="7c4ec-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c4ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c4ec-105">Wenn das Messagingsystem dies erfordert, ist der Transportanbieter für die Implementierung einer angemessenen Sicherheitsstufe für den Zugriff auf das Messagingsystem verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="7c4ec-105">If the messaging system requires it, the transport provider is responsible for implementing an appropriate level of security for access to the messaging system.</span></span> <span data-ttu-id="7c4ec-106">Jede eingehende oder ausgehende Nachricht, die über den MAPI-Spooler über einen Transportanbieter gesendet wird, wird im Kontext einer Anbieter Anmeldesitzung behandelt.</span><span class="sxs-lookup"><span data-stu-id="7c4ec-106">Each incoming or outgoing message sent through a transport provider by the MAPI spooler is handled in the context of a provider logon session.</span></span> <span data-ttu-id="7c4ec-107">Der Transportanbieter kann dem Benutzer ein Anmeldedialogfeld anzeigen, das die Anmeldeinformationen eines Benutzers anfordert, bevor eine solche Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7c4ec-107">The transport provider can display a logon dialog box to the user that prompts for a user's credentials before establishing such a connection.</span></span> <span data-ttu-id="7c4ec-108">Alternativ kann der Transportanbieter die zuvor eingegebenen Anmeldeinformationen des Benutzers im Secure-Eigenschaftsbereich eines Profil Abschnitts speichern und für den Zugriff ohne Eingabeaufforderungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c4ec-108">Alternatively, the transport provider can store the user's previously entered credentials in the secure property range within a profile section and use them for access without prompting.</span></span>
  
<span data-ttu-id="7c4ec-109">Berücksichtigen Sie beim Implementieren der Sicherheit Ihres Transportanbieters Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7c4ec-109">When implementing your transport provider's security, consider the following:</span></span>
  
- <span data-ttu-id="7c4ec-110">Bei mehreren installierten Dienstanbietern kann es eine Vielzahl von Namen und Kennwörtern geben, die einem Benutzer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7c4ec-110">With multiple installed service providers, there can be a multitude of names and passwords associated with a user.</span></span>
    
- <span data-ttu-id="7c4ec-111">MAPI ermöglicht mehrere Sitzungen mit mehreren Identitäten.</span><span class="sxs-lookup"><span data-stu-id="7c4ec-111">MAPI allows multiple sessions with multiple identities.</span></span> <span data-ttu-id="7c4ec-112">Anbieter werden aufgefordert, mehrere Sitzungen zu unterstützen, sind jedoch nicht dazu verpflichtet.</span><span class="sxs-lookup"><span data-stu-id="7c4ec-112">Providers are encouraged to support multiple sessions but are not required to do so.</span></span>
    
- <span data-ttu-id="7c4ec-113">Jede Sitzung mit einem Transportanbieter wird von MAPI mit einem diskreten Abschnitt im Profil des Benutzers verknüpft.</span><span class="sxs-lookup"><span data-stu-id="7c4ec-113">Each session with a transport provider is associated by MAPI with a discrete section in the user's profile.</span></span> <span data-ttu-id="7c4ec-114">Der Transportanbieter kann die [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) -Methode verwenden, um Zugriff auf diesen Abschnitt zu erhalten, der zum Speichern der dieser Sitzung zugeordneten Informationen, einschließlich der Anmeldeinformationen, verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7c4ec-114">The transport provider can use the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to gain access to this section, which can be used to store any information associated with this session, including credentials.</span></span> 
    
- <span data-ttu-id="7c4ec-115">Bei mehreren installierten Transportanbietern ist es nicht unbedingt wahr, dass der Benutzer nur eine einzige e-Mail-Adresse hat.</span><span class="sxs-lookup"><span data-stu-id="7c4ec-115">With multiple installed transport providers, it is not necessarily true that the user only has a single email address.</span></span> <span data-ttu-id="7c4ec-116">Ein Benutzer kann eine separate e-Mail-Adresse für jeden installierten Transportanbieter haben oder eine andere Adresse für jede Sitzung in einem einzelnen Anbieter haben.</span><span class="sxs-lookup"><span data-stu-id="7c4ec-116">A user can have a separate email address for each installed transport provider or can have a different address for each session on a single provider.</span></span>
    
<span data-ttu-id="7c4ec-117">Weitere Informationen zum Speichern von Anmeldeinformationen in Profil Abschnitten finden Sie unter [Message Services and Profiles](message-services-and-profiles.md) and [IProfSect: IMAPIProp](iprofsectimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="7c4ec-117">For more information about storing credentials in profile sections, see [Message Services and Profiles](message-services-and-profiles.md) and [IProfSect : IMAPIProp](iprofsectimapiprop.md).</span></span>
  

