---
title: Eigene Formularbibliotheken
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 546b45deaa856bbfa002797e491d9b47be0dd34a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581587"
---
# <a name="personal-form-libraries"></a><span data-ttu-id="d8b23-103">Eigene Formularbibliotheken</span><span class="sxs-lookup"><span data-stu-id="d8b23-103">Personal Form Libraries</span></span>

  
  
<span data-ttu-id="d8b23-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8b23-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8b23-105">Wie der Name schon sagt, enthalten persönliche Formularbibliotheken Formulare für einen bestimmten Benutzer von Interesse an.</span><span class="sxs-lookup"><span data-stu-id="d8b23-105">As its name suggests, personal form libraries contain forms of interest to a particular user.</span></span> <span data-ttu-id="d8b23-106">Ein Benutzer Persönliche Formularbibliothek ist der Formularbibliothek, die im Profil des Benutzers identifizierten Standard-Informationsspeicher zugeordnet. jedes Profil auf einer Arbeitsstation installiert können eine separate Standardspeicher und daher eine separate persönliche Formularbibliothek.</span><span class="sxs-lookup"><span data-stu-id="d8b23-106">A user's personal form library is the form library associated with the default message store identified in the user's profile; each profile installed on a workstation can use a separate default store, and therefore, a separate personal form library.</span></span> <span data-ttu-id="d8b23-107">Eine persönliche Formularbibliothek kann Kopien Formulare enthalten, die auch in anderen Formularbibliotheken zusätzlich zu anderen Formen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d8b23-107">A personal form library can contain copies of forms that are also contained in other form libraries in addition to other forms.</span></span>
  
<span data-ttu-id="d8b23-108">In der Tabelle verknüpfte Inhalt des Stammordners in Nachricht-Standardspeicher des Benutzers ist eine persönliche Formularbibliothek implementiert – ob, die auf einem Server oder lokal auf dem Computer des Benutzers befindet, ist unerheblich.</span><span class="sxs-lookup"><span data-stu-id="d8b23-108">A personal form library is implemented in the associated-contents table of the root folder in a user's default message store — whether that resides on a server or locally on the user's workstation is immaterial.</span></span> <span data-ttu-id="d8b23-109">Wenn Message-Standardspeicher des Benutzers auf dem Computer des Benutzers gespeichert ist, bieten persönliche Formularbibliotheken verbesserte Leistung durch Aktivieren von Clientanwendungen auf Formulare lokal anstelle von über das Netzwerk zugreifen.</span><span class="sxs-lookup"><span data-stu-id="d8b23-109">If the user's default message store is stored on the user's workstation, personal form libraries offer enhanced performance by enabling applications to access forms locally instead of over the network.</span></span> <span data-ttu-id="d8b23-110">Es wird auch angezeigt Formulare Offlinearbeit, Benutzern die kann auftreten, wenn Benutzer ihre Formulare auf tragbaren Computern mit ihnen zu übernehmen möchten und ohne Zugriff auf ein Netzwerk sind.</span><span class="sxs-lookup"><span data-stu-id="d8b23-110">It also makes forms available to users working offline, which can occur when users want to take their forms with them on portable computers and are without access to a network.</span></span>
  
<span data-ttu-id="d8b23-111">Die Eigenschaften und die zugrunde liegende Implementierung der persönlichen Formular Bibliothek Einträge enthalten eine "Container-ID"-Eigenschaft, die einen Master-Shape Container identifiziert, dem mit der lokale Eintrag synchronisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="d8b23-111">The properties and underlying implementation of personal form library entries include a "Container ID" property that identifies a master container that the local entry must be synchronized with.</span></span> <span data-ttu-id="d8b23-112">Dies kann den Bezeichner eines beliebigen Ordners sein, die Formulare enthält.</span><span class="sxs-lookup"><span data-stu-id="d8b23-112">This can be the identifier of an arbitrary folder that contains forms.</span></span> <span data-ttu-id="d8b23-113">Dies ist nützlich, wenn Sie einen benutzerdefiniertes Formular-Manager verwenden, der eine Art von organisationsweiten Formularbibliothek unterstützt. der Formular-Manager würde übernehmen synchronisieren die Formulare in der persönlichen Formularbibliothek und der gesamten Organisation Formularbibliothek gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d8b23-113">This is useful if you are using a custom form manager that supports some sort of organization-wide form library; the form manager would take care of synchronizing the forms stored in the personal form library and the organization-wide form library.</span></span> <span data-ttu-id="d8b23-114">Dies würde wahrscheinlich vorkommen, wenn der Formular-Manager geladen wurde, jedoch kann jederzeit theoretisch vorkommen.</span><span class="sxs-lookup"><span data-stu-id="d8b23-114">This would probably happen when the form manager was loaded, but could theoretically happen at any time.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d8b23-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8b23-115">See also</span></span>



[<span data-ttu-id="d8b23-116">MAPI-Formulare</span><span class="sxs-lookup"><span data-stu-id="d8b23-116">MAPI Forms</span></span>](mapi-forms.md)

