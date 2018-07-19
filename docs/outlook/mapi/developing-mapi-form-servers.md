---
title: Entwickeln von MAPI-Formularservern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 83d652f313e139b1c6bb628d1119edda03a70e23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791543"
---
# <a name="developing-mapi-form-servers"></a><span data-ttu-id="d6f6b-103">Entwickeln von MAPI-Formularservern</span><span class="sxs-lookup"><span data-stu-id="d6f6b-103">Developing MAPI Form Servers</span></span>

  
  
<span data-ttu-id="d6f6b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d6f6b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d6f6b-105">Dieser Abschnitt beschreibt den Prozess beim Erstellen von Forms Server ausführbare und Konfigurationsdateien für das Erstellen von benutzerdefinierter Formularen für MAPI-Formular.</span><span class="sxs-lookup"><span data-stu-id="d6f6b-105">This section describes the process of creating form server executable and form configuration files for creating custom MAPI forms.</span></span> <span data-ttu-id="d6f6b-106">Vor dem Lesen dieses Abschnitts, sollten Sie sich mit den Informationen im [MAPI-Formulare](mapi-forms.md)vertraut machen.</span><span class="sxs-lookup"><span data-stu-id="d6f6b-106">Before reading this section, you should familiarize yourself with the information in [MAPI Forms](mapi-forms.md).</span></span>
  
<span data-ttu-id="d6f6b-107">Entwickeln von einem Formular Server umfasst die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="d6f6b-107">Developing a form server includes the following steps:</span></span>
  
1. <span data-ttu-id="d6f6b-108">Entscheiden, welche Informationen des Formulars enthalten soll, und wählen Sie eine Gruppe von Eigenschaften, die diese Informationen enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="d6f6b-108">Deciding what information the form will contain and choosing a set of properties to hold that information.</span></span> <span data-ttu-id="d6f6b-109">Weitere Informationen finden Sie unter [Auswählen eines Formulars-Eigenschaft festgelegt](choosing-a-form-s-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="d6f6b-109">For more information, see [Choosing a Form's Property Set](choosing-a-form-s-property-set.md).</span></span>
    
2. <span data-ttu-id="d6f6b-110">Entwerfen eine Benutzeroberfläche, mit denen Benutzer die Eigenschaften des Formulars interagieren können.</span><span class="sxs-lookup"><span data-stu-id="d6f6b-110">Designing a user interface with which users can interact with the form's properties.</span></span>
    
3. <span data-ttu-id="d6f6b-111">Auswählen einer Nachrichtenklasse und Generieren einer eindeutigen Klassen-ID (CLSID).</span><span class="sxs-lookup"><span data-stu-id="d6f6b-111">Choosing a message class and generating a unique class identifier (CLSID).</span></span> <span data-ttu-id="d6f6b-112">Eine Übersicht über Nachrichtenklassen finden Sie unter [MAPI Message Classes](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="d6f6b-112">For an overview of message classes, see [MAPI Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="d6f6b-113">Weitere Informationen zu Nachrichtenklassen und Formulare finden Sie unter [Auswählen einer Nachrichtenklasse](choosing-a-message-class.md).</span><span class="sxs-lookup"><span data-stu-id="d6f6b-113">For more information about message classes and forms, see [Choosing a Message Class](choosing-a-message-class.md).</span></span>
    
4. <span data-ttu-id="d6f6b-114">Implementieren die erforderlichen Schnittstellen des MAPI-Formular als auch optionalen Schnittstellen, die Ihre Server bestimmten Formulars benötigt.</span><span class="sxs-lookup"><span data-stu-id="d6f6b-114">Implementing the required MAPI form interfaces, as well as any optional interfaces that your particular form server needs.</span></span> <span data-ttu-id="d6f6b-115">Weitere Informationen finden Sie unter [Writing Formularcode Server](writing-form-server-code.md).</span><span class="sxs-lookup"><span data-stu-id="d6f6b-115">For more information, see [Writing Form Server Code](writing-form-server-code.md).</span></span> 
    
5. <span data-ttu-id="d6f6b-116">Schreiben von Code für die Benutzeroberfläche zur Handhabung der Interaktion mit der Form-Objekt und die Eigenschaften des Benutzers verwendet das Formular.</span><span class="sxs-lookup"><span data-stu-id="d6f6b-116">Writing user interface code to handle the user's interaction with the form object and the properties the form uses.</span></span>
    
6. <span data-ttu-id="d6f6b-117">Erstellen eine Formular-Konfigurationsdatei für das Formular.</span><span class="sxs-lookup"><span data-stu-id="d6f6b-117">Creating a form configuration file for the form.</span></span> <span data-ttu-id="d6f6b-118">Weitere Informationen finden Sie unter [File Format des Formulars Konfigurationsdateien](file-format-of-form-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="d6f6b-118">For more information, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
    
7. <span data-ttu-id="d6f6b-119">Das Formular wird auf den Computern der Benutzer installiert.</span><span class="sxs-lookup"><span data-stu-id="d6f6b-119">Installing the form on users' computers.</span></span> <span data-ttu-id="d6f6b-120">Weitere Informationen finden Sie unter [Installieren eines Formulars in eine Bibliothek](installing-a-form-into-a-library.md).</span><span class="sxs-lookup"><span data-stu-id="d6f6b-120">For more information, see [Installing a Form into a Library](installing-a-form-into-a-library.md).</span></span>
    
<span data-ttu-id="d6f6b-121">Ausführen der Schritte 1 bis 5 wahrscheinlich gleichzeitig, anstatt sie in der Abfolge abschließen.</span><span class="sxs-lookup"><span data-stu-id="d6f6b-121">You will most likely perform steps 1 through 5 simultaneously rather than completing them in sequence.</span></span> <span data-ttu-id="d6f6b-122">Der Prozess der Entwicklung von einem Formular Server, wie viele Projekte programming, also keiner der in dem eine besonders gut definierte Sequenz vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d6f6b-122">The process of developing a form server, like many programming projects, is not one in which there is a particularly well-defined sequence.</span></span> <span data-ttu-id="d6f6b-123">Erstellen einer Konfigurationsdatei Formular ist beispielsweise dargestellt, wie die letzte Sekunde Schritt oben, aber wahrscheinlich Sie Ihre Konfiguration Formulardatei inkrementell erstellen und genauere Dies wird, wie Sie Features auf Ihrem Formular Server hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d6f6b-123">For example, creating a form configuration file is shown as the second-to-last step above, but you will probably create your form configuration file incrementally, and it will become more complete as you add features to your form server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d6f6b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6f6b-124">See also</span></span>



[<span data-ttu-id="d6f6b-125">MAPI-Konzepte (engl.)</span><span class="sxs-lookup"><span data-stu-id="d6f6b-125">MAPI Concepts</span></span>](mapi-concepts.md)

