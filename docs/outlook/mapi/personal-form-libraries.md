---
title: Persönliche Formularbibliotheken
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c84665077f9c8e02647a4d348042515366b0c090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420409"
---
# <a name="personal-form-libraries"></a><span data-ttu-id="0b464-103">Persönliche Formularbibliotheken</span><span class="sxs-lookup"><span data-stu-id="0b464-103">Personal Form Libraries</span></span>

  
  
<span data-ttu-id="0b464-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b464-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b464-105">Wie der Name schon sagt, enthalten persönliche Formularbibliotheken Formen, die für einen bestimmten Benutzer von Interesse sind.</span><span class="sxs-lookup"><span data-stu-id="0b464-105">As its name suggests, personal form libraries contain forms of interest to a particular user.</span></span> <span data-ttu-id="0b464-106">Die persönliche Formularbibliothek eines Benutzers ist die Formularbibliothek, die dem im Benutzerprofil identifizierten Standardnachrichtenspeicher zugeordnet ist. Jedes auf einer Arbeitsstation installierte Profil kann einen separaten Standardspeicher und somit eine separate persönliche Formularbibliothek verwenden.</span><span class="sxs-lookup"><span data-stu-id="0b464-106">A user's personal form library is the form library associated with the default message store identified in the user's profile; each profile installed on a workstation can use a separate default store, and therefore, a separate personal form library.</span></span> <span data-ttu-id="0b464-107">Eine persönliche Formularbibliothek kann Kopien von Formularen enthalten, die zusätzlich zu anderen Formularen auch in anderen Formularbibliotheken enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0b464-107">A personal form library can contain copies of forms that are also contained in other form libraries in addition to other forms.</span></span>
  
<span data-ttu-id="0b464-108">Eine persönliche Formularbibliothek wird im Inhaltsverzeichnis des Stammordners im Standardnachrichtenspeicher eines Benutzers implementiert – unabhängig davon, ob diese sich auf einem Server oder lokal auf der Arbeitsstation des Benutzers befindet, ist unerheblich.</span><span class="sxs-lookup"><span data-stu-id="0b464-108">A personal form library is implemented in the associated-contents table of the root folder in a user's default message store — whether that resides on a server or locally on the user's workstation is immaterial.</span></span> <span data-ttu-id="0b464-109">Wenn der Standardnachrichtenspeicher des Benutzers auf der Arbeitsstation des Benutzers gespeichert ist, bieten persönliche Formularbibliotheken eine verbesserte Leistung, indem Anwendungen den lokalen Zugriff auf Formulare statt über das Netzwerk ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0b464-109">If the user's default message store is stored on the user's workstation, personal form libraries offer enhanced performance by enabling applications to access forms locally instead of over the network.</span></span> <span data-ttu-id="0b464-110">Darüber hinaus stehen Benutzern, die offline arbeiten, Formulare zur Verfügung, die auftreten können, wenn Benutzer ihre Formulare auf tragbaren Computern mit sich nehmen möchten und keinen Zugriff auf ein Netzwerk haben.</span><span class="sxs-lookup"><span data-stu-id="0b464-110">It also makes forms available to users working offline, which can occur when users want to take their forms with them on portable computers and are without access to a network.</span></span>
  
<span data-ttu-id="0b464-111">Die Eigenschaften und die zugrunde liegende Implementierung persönlicher Formularbibliothekseinträge enthalten eine "Container-ID"-Eigenschaft, die einen Mastercontainer identifiziert, mit dem der lokale Eintrag synchronisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="0b464-111">The properties and underlying implementation of personal form library entries include a "Container ID" property that identifies a master container that the local entry must be synchronized with.</span></span> <span data-ttu-id="0b464-112">Dies kann der Bezeichner eines beliebigen Ordners sein, der Formulare enthält.</span><span class="sxs-lookup"><span data-stu-id="0b464-112">This can be the identifier of an arbitrary folder that contains forms.</span></span> <span data-ttu-id="0b464-113">Dies ist hilfreich, wenn Sie einen benutzerdefinierten Formular-Manager verwenden, der eine Art organisationsweite Formularbibliothek unterstützt. Der Formularmanager kümmert sich um die Synchronisierung der in der persönlichen Formularbibliothek und der organisationsweiten Formularbibliothek gespeicherten Formulare.</span><span class="sxs-lookup"><span data-stu-id="0b464-113">This is useful if you are using a custom form manager that supports some sort of organization-wide form library; the form manager would take care of synchronizing the forms stored in the personal form library and the organization-wide form library.</span></span> <span data-ttu-id="0b464-114">Dies würde wahrscheinlich passieren, wenn der Formular-Manager geladen wurde, aber theoretisch jederzeit geschehen.</span><span class="sxs-lookup"><span data-stu-id="0b464-114">This would probably happen when the form manager was loaded, but could theoretically happen at any time.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0b464-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b464-115">See also</span></span>



[<span data-ttu-id="0b464-116">MAPI-Formulare</span><span class="sxs-lookup"><span data-stu-id="0b464-116">MAPI Forms</span></span>](mapi-forms.md)

