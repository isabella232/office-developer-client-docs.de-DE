---
title: Formularverben
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: dbd08437dfdd38c3a43cbf12eae8710cc8e3661e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424028"
---
# <a name="form-verbs"></a><span data-ttu-id="c83fc-103">Formularverben</span><span class="sxs-lookup"><span data-stu-id="c83fc-103">Form verbs</span></span>

<span data-ttu-id="c83fc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c83fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c83fc-105">Die Benutzeroberfläche eines Formulars bietet normalerweise Menüelemente oder Steuerelemente, mit denen Benutzer eine Art von Aktion mit dem Formular ausführen können.</span><span class="sxs-lookup"><span data-stu-id="c83fc-105">A form's user interface typically offers menu items or controls that enable users to take some kind of action with the form.</span></span> <span data-ttu-id="c83fc-106">Diese Benutzeraktionen werden vom Formularserver ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c83fc-106">It is the form server's job to handle these user actions.</span></span> <span data-ttu-id="c83fc-107">Diese Schnittstelle wird mit standardmäßigen Win32-APIs implementiert; Writing One ist genau wie das Schreiben von anderen Schnittstellen für reguläre Win32-Programme.</span><span class="sxs-lookup"><span data-stu-id="c83fc-107">This interface is implemented using standard Win32 APIs; writing one is just like writing other interfaces for regular Win32 programs.</span></span>
  
<span data-ttu-id="c83fc-108">Häufig werden Benutzeraktionen mit Verben verknüpft.</span><span class="sxs-lookup"><span data-stu-id="c83fc-108">Often, user actions are associated with verbs.</span></span> <span data-ttu-id="c83fc-109">Ein Verb ist der Name für eine Aktion, die für eine bestimmte Nachrichtenklasse spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="c83fc-109">A verb is the name for an action that is specific to a certain message class.</span></span> <span data-ttu-id="c83fc-110">**Reply** ist beispielsweise ein Verb, das von vielen Formular Servern implementiert wird, von denen jede eine andere Interpretation dieses Verbs haben kann.</span><span class="sxs-lookup"><span data-stu-id="c83fc-110">For example, **Reply** is a verb that is implemented by many form servers, each of which may have a different interpretation of that verb.</span></span> <span data-ttu-id="c83fc-111">Verben werden manchmal auch als Befehle bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c83fc-111">Verbs are sometimes referred to as commands.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c83fc-112">Nicht alle Menüelemente und Steuerelemente in einem Formular entsprechen einem Verb.</span><span class="sxs-lookup"><span data-stu-id="c83fc-112">Not all menu items and controls on a form correspond to a verb.</span></span> <span data-ttu-id="c83fc-113">Beispielsweise entspricht eine **Abbrechen** -Schaltfläche nicht einem Abbrechen-Verb innerhalb des Formular Servers.</span><span class="sxs-lookup"><span data-stu-id="c83fc-113">For example, a **Cancel** button does not correspond to a Cancel verb within the form server.</span></span> <span data-ttu-id="c83fc-114">Verben sind in der Regelaktionen zugeordnet, die spezifisch für eine bestimmte Nachrichtenklasse oder eine Gruppe von Nachrichtenklassen sind.</span><span class="sxs-lookup"><span data-stu-id="c83fc-114">Usually, verbs are associated with actions that are specific to a particular message class or a set of message classes.</span></span> <span data-ttu-id="c83fc-115">Obwohl unterschiedliche Nachrichtenklassen unterschiedliche Verben unterstützen können, unterstützen alle mindestens das offene Verb, das die Benutzeroberfläche des Formulars anzeigt und mit den Eigenschaftenwerten der Nachricht lädt.</span><span class="sxs-lookup"><span data-stu-id="c83fc-115">Although different message classes can support different sets of verbs, all support at least the Open verb, which displays the form's user interface and loads it with the message's property values.</span></span> 
  
<span data-ttu-id="c83fc-116">Verben können keine Parameter annehmen.</span><span class="sxs-lookup"><span data-stu-id="c83fc-116">Verbs may take no parameters.</span></span> <span data-ttu-id="c83fc-117">Formulare, die Befehle mit Variablen Parametern exportieren, müssen die Automatisierungsmechanismen verwenden.</span><span class="sxs-lookup"><span data-stu-id="c83fc-117">Forms that export commands with variable parameters must use the Automation mechanisms.</span></span>
  
<span data-ttu-id="c83fc-118">Clients können mithilfe der [IMAPIFormInfo:: CalcVerbSet](imapiforminfo-calcverbset.md) -Methode, die vom MAPI-Formular-Manager implementiert wird, bestimmen, welche Verben von einer bestimmten Nachrichtenklasse unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c83fc-118">Clients can determine which verbs are supported by a particular message class through the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method, which is implemented by the MAPI form manager.</span></span> <span data-ttu-id="c83fc-119">Der Formular-Manager ruft diese Informationen aus der Konfigurationsdatei des Formulars ab.</span><span class="sxs-lookup"><span data-stu-id="c83fc-119">The form manager gets this information from the form's configuration file.</span></span> <span data-ttu-id="c83fc-120">Das von dieser Methode zurückgegebene Verb Set wird vom Client verwendet, um den Benutzer anzuzeigen, welche Befehle für eine Nachricht ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="c83fc-120">The verb set returned by this method is used by the client to show the user which commands can be executed on a message.</span></span> <span data-ttu-id="c83fc-121">Beispielsweise kann ein Client Benutzern ermöglichen, mit der rechten Maustaste auf eine Nachricht zu klicken, um Verben anzuzeigen, die für diese Nachricht gelten.</span><span class="sxs-lookup"><span data-stu-id="c83fc-121">For example, a client might enable users to click the right mouse button over a message to display verbs applicable to that message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c83fc-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c83fc-122">See also</span></span>

- [<span data-ttu-id="c83fc-123">MAPI-Formulare</span><span class="sxs-lookup"><span data-stu-id="c83fc-123">MAPI Forms</span></span>](mapi-forms.md)

