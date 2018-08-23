---
title: Übersicht über die MAPI-Adresse Adressbuch-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 855b145bcca8007601eb8e841665306d4c58982f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576561"
---
# <a name="mapi-address-book-provider-overview"></a><span data-ttu-id="74d7d-103">Übersicht über die MAPI-Adresse Adressbuch-Anbieter</span><span class="sxs-lookup"><span data-stu-id="74d7d-103">MAPI address book provider overview</span></span>
  
<span data-ttu-id="74d7d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74d7d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74d7d-105">Adressbuch Anbieter Handle Zugriff auf Verzeichnisinformationen.</span><span class="sxs-lookup"><span data-stu-id="74d7d-105">Address book providers handle access to directory information.</span></span> <span data-ttu-id="74d7d-106">Verzeichnisinformationen besteht aus Daten für zwei Arten von Nachrichtenempfängern: einzelne messaging-Benutzer und Gruppen von messaging-Benutzer, die häufig miteinander in Verteilerlisten behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="74d7d-106">Directory information consists of data for two types of message recipients: individual messaging users and groups of messaging users who are commonly addressed together in distribution lists.</span></span> <span data-ttu-id="74d7d-107">Je nach Art der Empfänger und die Adressbuchanbieter ist eine Vielzahl von Informationen, die verfügbar gemacht werden kann.</span><span class="sxs-lookup"><span data-stu-id="74d7d-107">Depending on the type of recipient and the address book provider, there is a wide range of information that can be made available.</span></span> <span data-ttu-id="74d7d-108">Beispielsweise speichern alle adressbuchanbietern implementierte Name, Adresse und Adresstyp des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="74d7d-108">For example, all address book providers store a recipient's name, address, and address type.</span></span>
  
<span data-ttu-id="74d7d-109">Jede Adressbuchanbieter organisiert diese Daten mithilfe eines oder mehrerer Container.</span><span class="sxs-lookup"><span data-stu-id="74d7d-109">Each address book provider organizes this data by using one or more containers.</span></span> <span data-ttu-id="74d7d-110">Die Anzahl und die Struktur der Container, hängt von der Adressbuchanbieter Implementierung ab.</span><span class="sxs-lookup"><span data-stu-id="74d7d-110">The number and structure of the containers depends on the address book provider's implementation.</span></span> <span data-ttu-id="74d7d-111">Beispielsweise eine Adressbuchanbieter möglicherweise einen einzelnen Container verwenden, um alle Informationen enthalten, eine andere möglicherweise einen Container der obersten Ebene, die Untercontainer enthält verwenden und eine dritte möglicherweise mehrere Container auf oberster Ebene, jede Betrieb Untercontainer verwenden.</span><span class="sxs-lookup"><span data-stu-id="74d7d-111">For example, one address book provider might use a single container to hold all of the information, another might use one top-level container that holds subcontainers, and a third might use several top-level containers, each holding subcontainers.</span></span> <span data-ttu-id="74d7d-112">Ein Container Adressbuchhierarchie kann sehr tiefe sein. Es gibt keine Begrenzung der Anzahl der Container, die verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="74d7d-112">An address book container hierarchy can be quite deep; there is no limit to the number of subcontainers that can be used.</span></span>
  
<span data-ttu-id="74d7d-113">Die folgende Abbildung zeigt eine typische MAPI-Struktur des Adressbuchs.</span><span class="sxs-lookup"><span data-stu-id="74d7d-113">The following illustration shows a typical MAPI address book organization.</span></span>
  
<span data-ttu-id="74d7d-114">**Adressbuchorganisation**</span><span class="sxs-lookup"><span data-stu-id="74d7d-114">**Address book organization**</span></span>
  
<span data-ttu-id="74d7d-115">![Struktur des Adressbuchs] (media/amapi_04.gif "Struktur des Adressbuchs")</span><span class="sxs-lookup"><span data-stu-id="74d7d-115">![Address book organization](media/amapi_04.gif "Address book organization")</span></span>
  
<span data-ttu-id="74d7d-116">MAPI integriert alle Informationen, die von den installierten adressbuchanbietern implementierte bereitgestellt wird, in einem einzigen Adressbuch, einer Präsentation eine einheitliche Ansicht an die Clientanwendung.</span><span class="sxs-lookup"><span data-stu-id="74d7d-116">MAPI integrates all the information supplied by the installed address book providers into a single address book, presenting a unified view to the client application.</span></span> <span data-ttu-id="74d7d-117">Die integrierte Liste zeigt die Container der obersten Ebene, die von den einzelnen der installierten adressbuchanbietern implementierte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="74d7d-117">The integrated list shows the top-level containers displayed by each of the installed address book providers.</span></span> <span data-ttu-id="74d7d-118">Die meisten adressbuchanbietern implementierte verfügbar machen nur ein paar Container (in der Regel von 1 bis 3) auf der obersten Ebene für die Einbeziehung in der obersten Ebene der MAPI-integrierte des Adressbuchs.</span><span class="sxs-lookup"><span data-stu-id="74d7d-118">Most address book providers expose only a few containers (typically one to three) at the top level for inclusion in the top level of the MAPI integrated address book.</span></span> <span data-ttu-id="74d7d-119">Beispielsweise kann ein Adressbuchanbieter verfügbar "Alle Benutzer" und "Lokale Benutzer" als zwei Container der obersten Ebene stellen.</span><span class="sxs-lookup"><span data-stu-id="74d7d-119">For example, an address book provider might make available "All Users" and "Local Users" as two containers at the top level.</span></span>
  
<span data-ttu-id="74d7d-120">Die Benutzer der Clientanwendungen können den Inhalt der Address Book Container anzeigen und ändern den Inhalt in einigen Fällen.</span><span class="sxs-lookup"><span data-stu-id="74d7d-120">The users of client applications can view the contents of address book containers and, in some cases, modify the contents.</span></span> <span data-ttu-id="74d7d-121">Mit unterschiedlichen Zugriffsebenen, je nach der Adressbuchanbieter können Address Book Containern erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="74d7d-121">Address book containers can be created with different access levels, depending on the address book provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="74d7d-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74d7d-122">See also</span></span>

- [<span data-ttu-id="74d7d-123">MAPI-Features und -Architektur</span><span class="sxs-lookup"><span data-stu-id="74d7d-123">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

