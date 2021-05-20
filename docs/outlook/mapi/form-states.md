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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429166"
---
# <a name="form-states"></a><span data-ttu-id="ce25f-103">Formularstatus</span><span class="sxs-lookup"><span data-stu-id="ce25f-103">Form states</span></span>

<span data-ttu-id="ce25f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce25f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce25f-105">Formularobjekte können sich in einem von fünf unterschiedlichen Zuständen unterscheiden, je nachdem, welche Methoden in ihnen aufgerufen wurden und ob Fehler bei der Ausführung dieser Methoden aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="ce25f-105">Form objects can be in one of five distinct states, depending on what methods have been called in them and whether any errors have occurred in performing those methods.</span></span> <span data-ttu-id="ce25f-106">Die Zustände werden in den folgenden Themen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="ce25f-106">The states are described in the following topics:</span></span>
  
- [<span data-ttu-id="ce25f-107">Nicht initialisierter Status</span><span class="sxs-lookup"><span data-stu-id="ce25f-107">Uninitialized State</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="ce25f-108">Normalzustand</span><span class="sxs-lookup"><span data-stu-id="ce25f-108">Normal State</span></span>](normal-state.md)
    
- [<span data-ttu-id="ce25f-109">NoScribble State</span><span class="sxs-lookup"><span data-stu-id="ce25f-109">NoScribble State</span></span>](noscribble-state.md)
    
- [<span data-ttu-id="ce25f-110">HandsOffAfterSave-Status</span><span class="sxs-lookup"><span data-stu-id="ce25f-110">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="ce25f-111">HandsOffFromNormal-Status</span><span class="sxs-lookup"><span data-stu-id="ce25f-111">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="ce25f-112">Die Zustände beziehen sich in erster Linie auf den Status der Daten im Formularobjekt.</span><span class="sxs-lookup"><span data-stu-id="ce25f-112">The states primarily relate to the status of the data in the form object.</span></span> <span data-ttu-id="ce25f-113">Die verschiedenen Zustände geben an, ob die Daten gespeichert werden müssen, ob das Formularobjekt Änderungen an den Daten zulassen soll und welchen Punkt das Speichern der Daten im Formular hat.</span><span class="sxs-lookup"><span data-stu-id="ce25f-113">The different states reflect whether the data needs to be saved, whether the form object should allow modifications to the data, and what point in the process of saving the data the form is in.</span></span> <span data-ttu-id="ce25f-114">Daher haben die Formularzustände und -übergänge zwischen ihnen mehr mit der Implementierung von [IPersistMessage : IUnknown-Schnittstellenmethoden](ipersistmessageiunknown.md) zu tun als alle anderen.</span><span class="sxs-lookup"><span data-stu-id="ce25f-114">As such, the form states and transitions between them have more to do with your form server's implementation of [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface methods than any other.</span></span> <span data-ttu-id="ce25f-115">Die Kenntnis dieser Zustände ist sehr nützlich für die ordnungsgemäße Implementierung der MAPI-Formularschnittstellen, die ihr Formularserver implementieren muss.</span><span class="sxs-lookup"><span data-stu-id="ce25f-115">Knowledge of these states is very useful for proper implementation of the MAPI form interfaces that your form server must implement.</span></span> 
  
<span data-ttu-id="ce25f-116">In den Themen in diesem Abschnitt werden die verschiedenen Zustände sowie die zulässigen Aktionen beschrieben, die Übergänge in andere Zustände verursachen.</span><span class="sxs-lookup"><span data-stu-id="ce25f-116">The topics in this section describe the various states, along with the allowed actions that cause transitions to other states.</span></span> <span data-ttu-id="ce25f-117">Übergänge, die in den Themen nicht aufgeführt sind, sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="ce25f-117">Any transitions not listed in the topics are not allowed.</span></span> <span data-ttu-id="ce25f-118">Wenn Ihre Formularobjekte nicht zulässige Übergänge zwischen Zuständen erstellen, verhalten sie sich nicht wie von Messagingclients erwartet und können unvorhersehbares Client- oder Formularobjektverhalten verursachen.</span><span class="sxs-lookup"><span data-stu-id="ce25f-118">If your form objects make disallowed transitions between states, they will not behave in the ways that messaging clients expect and could cause unpredictable client or form object behavior.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ce25f-119">Einige Zustandsübergänge hängen von Informationen aus früheren Zuzuständen ab.</span><span class="sxs-lookup"><span data-stu-id="ce25f-119">Some state transitions depend on information from previous states.</span></span> <span data-ttu-id="ce25f-120">Der Formularserver muss höchstwahrscheinlich ein Kennzeichen in seinen Formularobjekten implementieren, um anzugeben, ob die Werte der Eigenschaften der Nachricht geändert wurden, um spätere Statusänderungen zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="ce25f-120">Your form server will most likely have to implement a flag in its form objects to indicate whether the values of the message's properties have been changed to facilitate later state changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ce25f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce25f-121">See also</span></span>

- [<span data-ttu-id="ce25f-122">Entwickeln von MAPI-Formularservern</span><span class="sxs-lookup"><span data-stu-id="ce25f-122">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

