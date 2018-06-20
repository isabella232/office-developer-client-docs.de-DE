---
title: MAPI-Formular-Objekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb9107d9-ad5c-4264-a457-dea193597dc9
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 426d3d5787f4ef8cde2883c5e2eb3699dd664965
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792996"
---
# <a name="mapi-form-objects"></a><span data-ttu-id="bb43d-103">MAPI-Formular-Objekte</span><span class="sxs-lookup"><span data-stu-id="bb43d-103">MAPI Form Objects</span></span>

  
  
<span data-ttu-id="bb43d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bb43d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bb43d-105">Formular-Objekte werden von Servern, um bestimmte Nachrichten anzeigen und zulassen, dass Benutzer mit ihnen interagieren Formular dynamisch erstellt.</span><span class="sxs-lookup"><span data-stu-id="bb43d-105">Form objects are created dynamically by form servers in order to display specific messages and allow users to interact with them.</span></span> <span data-ttu-id="bb43d-106">Ein Form-Objekt ist daher eine Instanziierung der abgeleiteten Klasse von [IMAPIForm](imapiformiunknown.md) , die vom Formular Server implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="bb43d-106">A form object is, therefore, an instantiation of the class derived from [IMAPIForm](imapiformiunknown.md) that is implemented by the form server.</span></span> <span data-ttu-id="bb43d-107">Wenn eine Nachricht von eine anderen Clientanwendung geöffnet wird, erstellt der Formular-Server für die Nachrichtenklasse ein Form-Objekt, um die Meldung zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="bb43d-107">When a client application opens a message, the form server for that message class creates a form object to handle the message.</span></span> <span data-ttu-id="bb43d-108">Das Form-Objekt klicken Sie dann die Benutzeroberfläche erstellt und zeigt die Eigenschaften der Nachricht darin.</span><span class="sxs-lookup"><span data-stu-id="bb43d-108">The form object then creates its interface and displays the properties of the message in it.</span></span> <span data-ttu-id="bb43d-109">Das Form-Objekt und seine Schnittstelle bleibt bestehen, bis der Benutzer geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="bb43d-109">The form object and its interface persists until the user closes it.</span></span> <span data-ttu-id="bb43d-110">Das Form-Objekt verarbeitet Änderungen an die Werte der Eigenschaften der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="bb43d-110">The form object handles any changes to the values of the message's properties.</span></span> 
  
<span data-ttu-id="bb43d-111">Darüber hinaus definieren die Schnittstellen im MAPI-Formulars einen Mechanismus, mit dem ein Form-Objekt geladen und eine Reihe von Nachrichten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bb43d-111">Additionally, the MAPI form interfaces define a mechanism by which one form object can load and display a series of messages.</span></span> <span data-ttu-id="bb43d-112">Dies ist ein Mechanismus Effizienz, wie diese Erstellung der Nachrichtenobjekte und ihre Schnittstellen und unnötige Vernichtung vermieden wird.</span><span class="sxs-lookup"><span data-stu-id="bb43d-112">This is an efficiency mechanism, as it avoids needless destruction and creation of message objects and their interfaces.</span></span> <span data-ttu-id="bb43d-113">Auf Anforderung durch die messaging-Client eine andere Meldung geladen werden, sollte das Form-Objekt alle Änderungen auf die aktuelle Nachricht Eigenschaften zu speichern.</span><span class="sxs-lookup"><span data-stu-id="bb43d-113">When requested by the messaging client to load a different message, the form object should save any changes to the current message's properties.</span></span>
  
<span data-ttu-id="bb43d-114">Informationen zu einer Clientanwendung aus Sicht des Formular-Objekte finden Sie unter [MAPI benutzerdefinierte Formular-Objekte](mapi-custom-form-objects.md).</span><span class="sxs-lookup"><span data-stu-id="bb43d-114">For information on a client application's perspective of form objects, see [MAPI Custom Form Objects](mapi-custom-form-objects.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bb43d-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb43d-115">See also</span></span>



[<span data-ttu-id="bb43d-116">MAPI-Formulare</span><span class="sxs-lookup"><span data-stu-id="bb43d-116">MAPI Forms</span></span>](mapi-forms.md)

