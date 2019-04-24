---
title: Ordner Formularbibliotheken
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62b7480e-b3eb-45fb-b74d-62f1dc918a53
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ec12cf567dbbd8c1710f835a3c19369dd3626fd4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281557"
---
# <a name="folder-form-libraries"></a><span data-ttu-id="8dd6e-103">Ordner Formularbibliotheken</span><span class="sxs-lookup"><span data-stu-id="8dd6e-103">Folder Form Libraries</span></span>

  
  
<span data-ttu-id="8dd6e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8dd6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8dd6e-105">In einigen Fällen möchten Sie möglicherweise ein oder mehrere Formulare einem bestimmten Ordner zuordnen.</span><span class="sxs-lookup"><span data-stu-id="8dd6e-105">In some cases, you might want to associate one or more forms with a specific folder.</span></span> <span data-ttu-id="8dd6e-106">Mitarbeiter in Ihrer Organisation können beispielsweise über einen Statusberichts Ordner in Ihrem persönlichen Nachrichtenspeicher verfügen, um Fortschrittsberichte zu erstellen und zu speichern.</span><span class="sxs-lookup"><span data-stu-id="8dd6e-106">For example, employees in your organization could all have a Progress Report folder in their personal message store for creating and storing progress reports.</span></span> <span data-ttu-id="8dd6e-107">Da der Fortschrittsbericht spezifisch für den fortSchrittsBericht Ordner der einzelnen Benutzer ist, ist es möglicherweise nicht angemessen, das Fortschrittsbericht-Formular in der systemweiten Formularbibliothek zu speichern.</span><span class="sxs-lookup"><span data-stu-id="8dd6e-107">Because the progress report is specific to each user's Progress Report folder, it might not be appropriate to store the progress report form in the system wide form library.</span></span> <span data-ttu-id="8dd6e-108">Es kann jedoch eine Kopie des Statusberichts Formulars in der Tabelle mit den zugehörigen Inhalten des Statusberichts Ordners der einzelnen Benutzer aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="8dd6e-108">However, a copy of the progress report form can be kept in the associated-contents table of each user's Progress Report folder.</span></span> <span data-ttu-id="8dd6e-109">Dadurch wird der Benutzer auf die Verwendung von Fortschrittsberichts Formularen außerhalb des festgelegten Ordners beschränkt.</span><span class="sxs-lookup"><span data-stu-id="8dd6e-109">This restricts the user from using progress report forms outside of the designated folder.</span></span>
  
<span data-ttu-id="8dd6e-110">Konzeptionell gibt es eine Ordner Formularbibliothek für jeden Ordner in einem Nachrichtenspeicher, auch wenn keine Formularserver installiert sind.</span><span class="sxs-lookup"><span data-stu-id="8dd6e-110">Conceptually, there is one folder form library for every folder in a message store, even if no form servers are installed in it.</span></span> <span data-ttu-id="8dd6e-111">Ordner Formularbibliotheken werden wie andere Formularbibliotheken implementiert – Sie werden als verknüpfte Inhaltstabellen im alternativen Teil des Ordners gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8dd6e-111">Folder form libraries are implemented like other form libraries — they are stored as associated-contents tables in the alternate part of the folder.</span></span> <span data-ttu-id="8dd6e-112">Da Ordner Formularbibliotheken im Ordner enthalten sind, werden Sie zusammen mit dem übergeordneten Ordner in Kopiervorgängen kopiert.</span><span class="sxs-lookup"><span data-stu-id="8dd6e-112">Because folder form libraries are contained in the folder, they are copied along with their parent folder in copy operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8dd6e-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8dd6e-113">See also</span></span>



[<span data-ttu-id="8dd6e-114">MAPI-Formulare</span><span class="sxs-lookup"><span data-stu-id="8dd6e-114">MAPI Forms</span></span>](mapi-forms.md)

