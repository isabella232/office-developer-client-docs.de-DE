---
title: Formular Verben
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1ecc80feec2b0a86f35d03f1ca4f75ea9ff094e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791723"
---
# <a name="form-verbs"></a><span data-ttu-id="8300f-103">Formular Verben</span><span class="sxs-lookup"><span data-stu-id="8300f-103">Form verbs</span></span>

<span data-ttu-id="8300f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8300f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8300f-105">Benutzeroberfläche des Formulars bietet in der Regel Menüelemente oder Steuerelemente, mit denen Benutzer die verschiedenste Aktion mit dem Formular.</span><span class="sxs-lookup"><span data-stu-id="8300f-105">A form's user interface typically offers menu items or controls that enable users to take some kind of action with the form.</span></span> <span data-ttu-id="8300f-106">Es ist dem Formular Server Auftrag an diese Benutzeraktionen zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="8300f-106">It is the form server's job to handle these user actions.</span></span> <span data-ttu-id="8300f-107">Diese Schnittstelle wird mit standard Win32-APIs implementiert. Schreiben einer verhält sich wie andere Schnittstellen für regulären Win32-Programme schreiben.</span><span class="sxs-lookup"><span data-stu-id="8300f-107">This interface is implemented using standard Win32 APIs; writing one is just like writing other interfaces for regular Win32 programs.</span></span>
  
<span data-ttu-id="8300f-108">Oft sind Benutzeraktionen Verben zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="8300f-108">Often, user actions are associated with verbs.</span></span> <span data-ttu-id="8300f-109">Ein Verb ist der Name für eine Aktion, die speziell für eine bestimmte Nachrichtenklasse ist.</span><span class="sxs-lookup"><span data-stu-id="8300f-109">A verb is the name for an action that is specific to a certain message class.</span></span> <span data-ttu-id="8300f-110">Beispielsweise ist **Antwort** ein Verb, die jeweils eine unterschiedliche Interpretation von diesem Verb möglicherweise viele Formular Server implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="8300f-110">For example, **Reply** is a verb that is implemented by many form servers, each of which may have a different interpretation of that verb.</span></span> <span data-ttu-id="8300f-111">Verben werden manchmal als Befehle bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8300f-111">Verbs are sometimes referred to as commands.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8300f-112">Nicht alle Menüelemente und Steuerelemente eines Formulars entsprechen ein Verb.</span><span class="sxs-lookup"><span data-stu-id="8300f-112">Not all menu items and controls on a form correspond to a verb.</span></span> <span data-ttu-id="8300f-113">Beispielsweise entspricht eine Schaltfläche **Abbrechen** nicht abbrechen Verb innerhalb des Servers Formular.</span><span class="sxs-lookup"><span data-stu-id="8300f-113">For example, a **Cancel** button does not correspond to a Cancel verb within the form server.</span></span> <span data-ttu-id="8300f-114">In der Regel Verben, die Aktionen, die speziell für eine bestimmte Nachrichtenklasse oder eine Gruppe von Nachrichtenklassen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8300f-114">Usually, verbs are associated with actions that are specific to a particular message class or a set of message classes.</span></span> <span data-ttu-id="8300f-115">Obwohl unterschiedliche Nachrichtenklassen verschiedene Sätze von Verben unterstützen können, unterstützen das Open Verb, das Benutzeroberfläche des Formulars angezeigt und lädt ihn mit der Nachricht Eigenschaftswerte mindestens.</span><span class="sxs-lookup"><span data-stu-id="8300f-115">Although different message classes can support different sets of verbs, all support at least the Open verb, which displays the form's user interface and loads it with the message's property values.</span></span> 
  
<span data-ttu-id="8300f-116">Verben können keine Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8300f-116">Verbs may take no parameters.</span></span> <span data-ttu-id="8300f-117">Formulare, die Befehle mit Variable Parameter exportieren müssen die Automatisierung Mechanismen verwenden.</span><span class="sxs-lookup"><span data-stu-id="8300f-117">Forms that export commands with variable parameters must use the Automation mechanisms.</span></span>
  
<span data-ttu-id="8300f-118">Clients können ermitteln, welche Verben von einer bestimmten Nachrichtenklasse über die Methode [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) unterstützt werden die von der MAPI-Formular-Manager implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="8300f-118">Clients can determine which verbs are supported by a particular message class through the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method, which is implemented by the MAPI form manager.</span></span> <span data-ttu-id="8300f-119">Der Formular-Manager ruft diese Informationen aus der Konfigurationsdatei des Formulars ab.</span><span class="sxs-lookup"><span data-stu-id="8300f-119">The form manager gets this information from the form's configuration file.</span></span> <span data-ttu-id="8300f-120">Der Verb Satz von dieser Methode zurückgegebene wird vom Client verwendet, um dem Benutzer anzuzeigen, welche Befehle für eine Nachricht ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="8300f-120">The verb set returned by this method is used by the client to show the user which commands can be executed on a message.</span></span> <span data-ttu-id="8300f-121">Beispielsweise kann ein Client Benutzer über eine Meldung an Verben für die Nachricht der rechten Maustaste auf aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8300f-121">For example, a client might enable users to click the right mouse button over a message to display verbs applicable to that message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8300f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8300f-122">See also</span></span>

- [<span data-ttu-id="8300f-123">MAPI-Formulare</span><span class="sxs-lookup"><span data-stu-id="8300f-123">MAPI Forms</span></span>](mapi-forms.md)

