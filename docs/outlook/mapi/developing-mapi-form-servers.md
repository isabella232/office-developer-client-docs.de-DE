---
title: Entwickeln von MAPI-Formular Servern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 63aa9db19c901f47004a7fe52d906846f44b8883
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338528"
---
# <a name="developing-mapi-form-servers"></a><span data-ttu-id="3789a-103">Entwickeln von MAPI-Formular Servern</span><span class="sxs-lookup"><span data-stu-id="3789a-103">Developing MAPI Form Servers</span></span>

  
  
<span data-ttu-id="3789a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3789a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3789a-105">In diesem Abschnitt wird das Erstellen von ausführbaren Formularserver-und Formular Konfigurationsdateien zum Erstellen benutzerdefinierter MAPI-Formulare beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3789a-105">This section describes the process of creating form server executable and form configuration files for creating custom MAPI forms.</span></span> <span data-ttu-id="3789a-106">Bevor Sie diesen Abschnitt lesen, sollten Sie sich mit den Informationen in [MAPI-Formularen](mapi-forms.md)vertraut machen.</span><span class="sxs-lookup"><span data-stu-id="3789a-106">Before reading this section, you should familiarize yourself with the information in [MAPI Forms](mapi-forms.md).</span></span>
  
<span data-ttu-id="3789a-107">Die Entwicklung eines Formular Servers umfasst die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="3789a-107">Developing a form server includes the following steps:</span></span>
  
1. <span data-ttu-id="3789a-108">Entscheiden Sie, welche Informationen das Formular enthalten soll, und wählen Sie eine Reihe von Eigenschaften aus, um diese Informationen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="3789a-108">Deciding what information the form will contain and choosing a set of properties to hold that information.</span></span> <span data-ttu-id="3789a-109">Weitere Informationen finden Sie unter [Auswählen eines Formulareigenschaften Satzes](choosing-a-form-s-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="3789a-109">For more information, see [Choosing a Form's Property Set](choosing-a-form-s-property-set.md).</span></span>
    
2. <span data-ttu-id="3789a-110">Entwerfen einer Benutzeroberfläche, mit der Benutzer mit den Eigenschaften des Formulars interagieren können.</span><span class="sxs-lookup"><span data-stu-id="3789a-110">Designing a user interface with which users can interact with the form's properties.</span></span>
    
3. <span data-ttu-id="3789a-111">Auswählen einer Nachrichtenklasse und Generieren einer eindeutigen Klassen-ID (CLSID).</span><span class="sxs-lookup"><span data-stu-id="3789a-111">Choosing a message class and generating a unique class identifier (CLSID).</span></span> <span data-ttu-id="3789a-112">Eine Übersicht über Nachrichtenklassen finden Sie unter [MAPI Message Classes](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="3789a-112">For an overview of message classes, see [MAPI Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="3789a-113">Weitere Informationen zu Nachrichtenklassen und-Formularen finden Sie unter [Auswählen einer Nachrichtenklasse](choosing-a-message-class.md).</span><span class="sxs-lookup"><span data-stu-id="3789a-113">For more information about message classes and forms, see [Choosing a Message Class](choosing-a-message-class.md).</span></span>
    
4. <span data-ttu-id="3789a-114">Implementieren der erforderlichen MAPI-Formular Schnittstellen sowie aller optionalen Schnittstellen, die für Ihren speziellen Formularserver erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="3789a-114">Implementing the required MAPI form interfaces, as well as any optional interfaces that your particular form server needs.</span></span> <span data-ttu-id="3789a-115">Weitere Informationen finden Sie unter [Schreiben von Formular Server Code](writing-form-server-code.md).</span><span class="sxs-lookup"><span data-stu-id="3789a-115">For more information, see [Writing Form Server Code](writing-form-server-code.md).</span></span> 
    
5. <span data-ttu-id="3789a-116">Schreiben von Benutzeroberflächencode, um die Interaktion des Benutzers mit dem Form-Objekt und den vom Formular verwendeten Eigenschaften zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="3789a-116">Writing user interface code to handle the user's interaction with the form object and the properties the form uses.</span></span>
    
6. <span data-ttu-id="3789a-117">Erstellen einer Formular Konfigurationsdatei für das Formular.</span><span class="sxs-lookup"><span data-stu-id="3789a-117">Creating a form configuration file for the form.</span></span> <span data-ttu-id="3789a-118">Weitere Informationen finden Sie unter [Datei Format von Formular Konfigurationsdateien](file-format-of-form-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="3789a-118">For more information, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
    
7. <span data-ttu-id="3789a-119">Installieren des Formulars auf Benutzercomputern.</span><span class="sxs-lookup"><span data-stu-id="3789a-119">Installing the form on users' computers.</span></span> <span data-ttu-id="3789a-120">Weitere Informationen finden Sie unter [Installieren eines Formulars in einer Bibliothek](installing-a-form-into-a-library.md).</span><span class="sxs-lookup"><span data-stu-id="3789a-120">For more information, see [Installing a Form into a Library](installing-a-form-into-a-library.md).</span></span>
    
<span data-ttu-id="3789a-121">Sie werden die Schritte 1 bis 5 höchstwahrscheinlich gleichzeitig ausführen, statt Sie nacheinander abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="3789a-121">You will most likely perform steps 1 through 5 simultaneously rather than completing them in sequence.</span></span> <span data-ttu-id="3789a-122">Der Prozess der Entwicklung eines Formular Servers ist, wie viele Programmierprojekte, nicht eine, in der es eine besonders gut definierte Sequenz gibt.</span><span class="sxs-lookup"><span data-stu-id="3789a-122">The process of developing a form server, like many programming projects, is not one in which there is a particularly well-defined sequence.</span></span> <span data-ttu-id="3789a-123">Beispielsweise wird das Erstellen einer Formular Konfigurationsdatei als der vorletzte Schritt oben angezeigt, aber Sie erstellen Ihre Formular Konfigurationsdatei wahrscheinlich inkrementell, und Sie wird umfassender, wenn Sie Ihrem Formularserver Features hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3789a-123">For example, creating a form configuration file is shown as the second-to-last step above, but you will probably create your form configuration file incrementally, and it will become more complete as you add features to your form server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3789a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3789a-124">See also</span></span>



[<span data-ttu-id="3789a-125">MAPI-Konzepte (engl.)</span><span class="sxs-lookup"><span data-stu-id="3789a-125">MAPI Concepts</span></span>](mapi-concepts.md)

