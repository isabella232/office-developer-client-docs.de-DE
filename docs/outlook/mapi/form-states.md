---
title: Formular Staaten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 969aca6fd37f237a607df36cc58f249828449e27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791749"
---
# <a name="form-states"></a><span data-ttu-id="4cbcd-103">Formular Staaten</span><span class="sxs-lookup"><span data-stu-id="4cbcd-103">Form states</span></span>

<span data-ttu-id="4cbcd-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4cbcd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4cbcd-105">Formular-Objekte können in eine der fünf verschiedenen Status, je nach welche Methoden werden aufgerufen wurden und ob Fehler aufgetreten sind, in diese Methoden ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4cbcd-105">Form objects can be in one of five distinct states, depending on what methods have been called in them and whether any errors have occurred in performing those methods.</span></span> <span data-ttu-id="4cbcd-106">In den folgenden Themen werden die Zustände beschrieben:</span><span class="sxs-lookup"><span data-stu-id="4cbcd-106">The states are described in the following topics:</span></span>
  
- [<span data-ttu-id="4cbcd-107">Nicht initialisierten Zustand</span><span class="sxs-lookup"><span data-stu-id="4cbcd-107">Uninitialized State</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="4cbcd-108">Normalzustand</span><span class="sxs-lookup"><span data-stu-id="4cbcd-108">Normal State</span></span>](normal-state.md)
    
- [<span data-ttu-id="4cbcd-109">NoScribble Zustand</span><span class="sxs-lookup"><span data-stu-id="4cbcd-109">NoScribble State</span></span>](noscribble-state.md)
    
- [<span data-ttu-id="4cbcd-110">HandsOffAfterSave Zustand</span><span class="sxs-lookup"><span data-stu-id="4cbcd-110">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="4cbcd-111">HandsOffFromNormal Zustand</span><span class="sxs-lookup"><span data-stu-id="4cbcd-111">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="4cbcd-112">Die Zustände beziehen sich hauptsächlich auf den Status der Daten in das Form-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4cbcd-112">The states primarily relate to the status of the data in the form object.</span></span> <span data-ttu-id="4cbcd-113">Die unterschiedlichen Zustände anzugeben, ob die Daten gespeichert werden müssen, ob das Form-Objekt Änderungen an welchem Punkt beim Speichern der Daten, die darf, denen in das Formular befindet, und die Daten.</span><span class="sxs-lookup"><span data-stu-id="4cbcd-113">The different states reflect whether the data needs to be saved, whether the form object should allow modifications to the data, and what point in the process of saving the data the form is in.</span></span> <span data-ttu-id="4cbcd-114">Als solche Formular Zustände und Übergänge zwischen diesen stärker mit Ihrem Formular Server Implementierung von [IPersistMessage: IUnknown](ipersistmessageiunknown.md) Schnittstellenmethoden als andere.</span><span class="sxs-lookup"><span data-stu-id="4cbcd-114">As such, the form states and transitions between them have more to do with your form server's implementation of [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface methods than any other.</span></span> <span data-ttu-id="4cbcd-115">Kenntnisse in dieser Zustände ist sehr nützlich für eine ordnungsgemäße Implementierung der MAPI-Formulars Schnittstellen, die der Formular Server implementiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="4cbcd-115">Knowledge of these states is very useful for proper implementation of the MAPI form interfaces that your form server must implement.</span></span> 
  
<span data-ttu-id="4cbcd-116">In den Themen in diesem Abschnitt beschreiben die verschiedenen Status, zusammen mit den zulässigen Aktionen, die dazu führen, in anderen Zustände wechselt dass.</span><span class="sxs-lookup"><span data-stu-id="4cbcd-116">The topics in this section describe the various states, along with the allowed actions that cause transitions to other states.</span></span> <span data-ttu-id="4cbcd-117">Alle Übergänge, die nicht in den Themen aufgeführt sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="4cbcd-117">Any transitions not listed in the topics are not allowed.</span></span> <span data-ttu-id="4cbcd-118">Wenn Ihr Formularobjekte nicht zulässige Übergänge zwischen Zuständen vornehmen, werden sie nicht Weise Verhalten, messaging-Clients auf Sie zukommt und unvorhersehbares Verhalten der Clients oder Form-Objekt verursachen.</span><span class="sxs-lookup"><span data-stu-id="4cbcd-118">If your form objects make disallowed transitions between states, they will not behave in the ways that messaging clients expect and could cause unpredictable client or form object behavior.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4cbcd-119">Einige Statusübergänge hängen von Informationen aus der vorherigen Status.</span><span class="sxs-lookup"><span data-stu-id="4cbcd-119">Some state transitions depend on information from previous states.</span></span> <span data-ttu-id="4cbcd-120">Ihr Formular Server muss in den meisten Fällen implementieren Sie ein Flag in Formularobjekte anzugeben, ob die Werte der Eigenschaften der Nachricht ändert sich höher vereinfachen geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="4cbcd-120">Your form server will most likely have to implement a flag in its form objects to indicate whether the values of the message's properties have been changed to facilitate later state changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4cbcd-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cbcd-121">See also</span></span>

- [<span data-ttu-id="4cbcd-122">Entwickeln von MAPI-Formular-Servern</span><span class="sxs-lookup"><span data-stu-id="4cbcd-122">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

