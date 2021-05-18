---
title: Ordnerformularbibliotheken
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62b7480e-b3eb-45fb-b74d-62f1dc918a53
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ec12cf567dbbd8c1710f835a3c19369dd3626fd4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414284"
---
# <a name="folder-form-libraries"></a><span data-ttu-id="63e13-103">Ordnerformularbibliotheken</span><span class="sxs-lookup"><span data-stu-id="63e13-103">Folder Form Libraries</span></span>

  
  
<span data-ttu-id="63e13-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63e13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63e13-105">In einigen Fällen können Sie einem bestimmten Ordner ein oder mehrere Formulare zuordnen.</span><span class="sxs-lookup"><span data-stu-id="63e13-105">In some cases, you might want to associate one or more forms with a specific folder.</span></span> <span data-ttu-id="63e13-106">Beispielsweise könnten Mitarbeiter in Ihrer Organisation alle einen Statusberichtsordner in ihrem persönlichen Nachrichtenspeicher zum Erstellen und Speichern von Fortschrittsberichten haben.</span><span class="sxs-lookup"><span data-stu-id="63e13-106">For example, employees in your organization could all have a Progress Report folder in their personal message store for creating and storing progress reports.</span></span> <span data-ttu-id="63e13-107">Da der Fortschrittsbericht für den Statusberichtsordner der einzelnen Benutzer spezifisch ist, ist es möglicherweise nicht sinnvoll, das Statusberichtsformular in der systemweiten Formularbibliothek zu speichern.</span><span class="sxs-lookup"><span data-stu-id="63e13-107">Because the progress report is specific to each user's Progress Report folder, it might not be appropriate to store the progress report form in the system wide form library.</span></span> <span data-ttu-id="63e13-108">Eine Kopie des Statusberichtsformulars kann jedoch im Inhaltsverzeichnis des Statusberichtsordners der einzelnen Benutzer aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="63e13-108">However, a copy of the progress report form can be kept in the associated-contents table of each user's Progress Report folder.</span></span> <span data-ttu-id="63e13-109">Dadurch wird der Benutzer an der Verwendung von Fortschrittsberichtsformularen außerhalb des angegebenen Ordners eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="63e13-109">This restricts the user from using progress report forms outside of the designated folder.</span></span>
  
<span data-ttu-id="63e13-110">Konzeptionell gibt es eine Ordnerformularbibliothek für jeden Ordner in einem Nachrichtenspeicher, auch wenn keine Formularserver installiert sind.</span><span class="sxs-lookup"><span data-stu-id="63e13-110">Conceptually, there is one folder form library for every folder in a message store, even if no form servers are installed in it.</span></span> <span data-ttu-id="63e13-111">Ordnerformularbibliotheken werden wie andere Formularbibliotheken implementiert– sie werden als Tabellen mit zugeordneten Inhalten im alternativen Teil des Ordners gespeichert.</span><span class="sxs-lookup"><span data-stu-id="63e13-111">Folder form libraries are implemented like other form libraries — they are stored as associated-contents tables in the alternate part of the folder.</span></span> <span data-ttu-id="63e13-112">Da Ordnerformularbibliotheken im Ordner enthalten sind, werden sie zusammen mit ihrem übergeordneten Ordner in Kopiervorgänge kopiert.</span><span class="sxs-lookup"><span data-stu-id="63e13-112">Because folder form libraries are contained in the folder, they are copied along with their parent folder in copy operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="63e13-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63e13-113">See also</span></span>



[<span data-ttu-id="63e13-114">MAPI-Formulare</span><span class="sxs-lookup"><span data-stu-id="63e13-114">MAPI Forms</span></span>](mapi-forms.md)

