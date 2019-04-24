---
title: Formularstatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 61d20ff7010151a82c53cafc69270e6925796a5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327517"
---
# <a name="form-states"></a><span data-ttu-id="b3f54-103">Formularstatus</span><span class="sxs-lookup"><span data-stu-id="b3f54-103">Form states</span></span>

<span data-ttu-id="b3f54-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3f54-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3f54-105">Formularobjekte können sich in einem von fünf unterschiedlichen Status befinden, je nachdem, welche Methoden in diesen aufgerufen wurden und ob beim Ausführen dieser Methoden Fehler aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="b3f54-105">Form objects can be in one of five distinct states, depending on what methods have been called in them and whether any errors have occurred in performing those methods.</span></span> <span data-ttu-id="b3f54-106">Die Zustände werden in den folgenden Themen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="b3f54-106">The states are described in the following topics:</span></span>
  
- [<span data-ttu-id="b3f54-107">Nicht initialisierter Status</span><span class="sxs-lookup"><span data-stu-id="b3f54-107">Uninitialized State</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="b3f54-108">Normaler Status</span><span class="sxs-lookup"><span data-stu-id="b3f54-108">Normal State</span></span>](normal-state.md)
    
- [<span data-ttu-id="b3f54-109">Status "noScribble"</span><span class="sxs-lookup"><span data-stu-id="b3f54-109">NoScribble State</span></span>](noscribble-state.md)
    
- [<span data-ttu-id="b3f54-110">HandsOffAfterSave-Status</span><span class="sxs-lookup"><span data-stu-id="b3f54-110">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="b3f54-111">Status "handsofffromnormal-Status</span><span class="sxs-lookup"><span data-stu-id="b3f54-111">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="b3f54-112">Die Zustände beziehen sich in erster Linie auf den Status der Daten im Form-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b3f54-112">The states primarily relate to the status of the data in the form object.</span></span> <span data-ttu-id="b3f54-113">Die verschiedenen Statusangaben geben an, ob die Daten gespeichert werden müssen, ob das Form-Objektänderungen an den Daten zulassen soll und wie die Daten, in denen das Formular gespeichert ist, in den Prozess eingespart werden.</span><span class="sxs-lookup"><span data-stu-id="b3f54-113">The different states reflect whether the data needs to be saved, whether the form object should allow modifications to the data, and what point in the process of saving the data the form is in.</span></span> <span data-ttu-id="b3f54-114">Daher haben die Formular Zustände und Übergänge zwischen diesen mehr mit der Implementierung der [IPersistMessage: IUnknown](ipersistmessageiunknown.md) -Schnittstellenmethoden durch den Formularserver als alle anderen.</span><span class="sxs-lookup"><span data-stu-id="b3f54-114">As such, the form states and transitions between them have more to do with your form server's implementation of [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface methods than any other.</span></span> <span data-ttu-id="b3f54-115">Die Kenntnis dieser Zustände ist sehr nützlich für die ordnungsgemäße Implementierung der MAPI-Formular Schnittstellen, die der Formularserver implementieren muss.</span><span class="sxs-lookup"><span data-stu-id="b3f54-115">Knowledge of these states is very useful for proper implementation of the MAPI form interfaces that your form server must implement.</span></span> 
  
<span data-ttu-id="b3f54-116">In den Themen in diesem Abschnitt werden die verschiedenen Status zusammen mit den zulässigen Aktionen beschrieben, die Übergänge zu anderen Zuständen verursachen.</span><span class="sxs-lookup"><span data-stu-id="b3f54-116">The topics in this section describe the various states, along with the allowed actions that cause transitions to other states.</span></span> <span data-ttu-id="b3f54-117">Alle Übergänge, die nicht in den Themen aufgeführt sind, sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="b3f54-117">Any transitions not listed in the topics are not allowed.</span></span> <span data-ttu-id="b3f54-118">Wenn Ihre Formularobjekte nicht zulässige Übergänge zwischen Zuständen vornehmen, Verhalten Sie sich nicht auf die Art und Weise, wie Messaging-Clients erwarten, und können zu unvorhersehbaren Client-oder Formularobjekt Verhalten führen.</span><span class="sxs-lookup"><span data-stu-id="b3f54-118">If your form objects make disallowed transitions between states, they will not behave in the ways that messaging clients expect and could cause unpredictable client or form object behavior.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b3f54-119">Einige Statusübergänge hängen von Informationen aus früheren Status ab.</span><span class="sxs-lookup"><span data-stu-id="b3f54-119">Some state transitions depend on information from previous states.</span></span> <span data-ttu-id="b3f54-120">Der Formularserver muss höchstwahrscheinlich ein Flag in seinen Form-Objekten implementieren, um anzugeben, ob die Werte der Eigenschaften der Nachricht geändert wurden, um spätere Statusänderungen zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="b3f54-120">Your form server will most likely have to implement a flag in its form objects to indicate whether the values of the message's properties have been changed to facilitate later state changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b3f54-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3f54-121">See also</span></span>

- [<span data-ttu-id="b3f54-122">Entwickeln von MAPI-Formular Servern</span><span class="sxs-lookup"><span data-stu-id="b3f54-122">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

