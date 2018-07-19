---
title: Installieren eines Formulars in einer Bibliothek
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 54b2dece31937b1ff233d4d1e7d8bbc198bfe118
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792705"
---
# <a name="installing-a-form-into-a-library"></a><span data-ttu-id="c2921-103">Installieren eines Formulars in einer Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c2921-103">Installing a Form into a Library</span></span>

  
  
<span data-ttu-id="c2921-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c2921-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c2921-105">Der standardmäßigen MAPI Formular-Manager mit dem Windows SDK bereitgestellte bietet keine Benutzeroberfläche für die Installation von Formularen in die verschiedenen Formularbibliotheken.</span><span class="sxs-lookup"><span data-stu-id="c2921-105">The default MAPI form manager supplied with the Windows SDK does not provide a user interface for installing forms in the various form libraries.</span></span> <span data-ttu-id="c2921-106">Aus diesem Grund müssen Sie eine kleine Anwendung erstellen – oder detaillierte Anweisungen –, dass Benutzer verwenden können, um das Formular zu installieren.</span><span class="sxs-lookup"><span data-stu-id="c2921-106">Because of this, you will have to create a small application — or detailed set of instructions — that users can use to install the form.</span></span>
  
<span data-ttu-id="c2921-107">Wenn Sie eine Installation Anwendung implementieren, muss der Reihe von Aktionen es führen Sie zum Installieren eines Formulars in einem Ordner zugeordneten Inhalt Tabelle lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c2921-107">If you implement an installation application, the series of actions it must perform to install a form into a folder's associated contents table are as follows:</span></span>
  
1. <span data-ttu-id="c2921-108">Rufen Sie die [MAPIOpenFormMgr](mapiopenformmgr.md) -Funktion zum Öffnen des Formulars Manager.</span><span class="sxs-lookup"><span data-stu-id="c2921-108">Call the [MAPIOpenFormMgr](mapiopenformmgr.md) function to open the form manager.</span></span> 
    
2. <span data-ttu-id="c2921-109">Verwenden Sie [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) oder [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) -Methode, um auszuwählen, und öffnen Sie den Zielcontainer für das Formular.</span><span class="sxs-lookup"><span data-stu-id="c2921-109">Use [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) or [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to select and open the target container for the form.</span></span> 
    
3. <span data-ttu-id="c2921-110">Verwenden Sie die [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) -Funktion, um das Formular zu installieren.</span><span class="sxs-lookup"><span data-stu-id="c2921-110">Use the [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) function to install the form.</span></span> 
    
    <span data-ttu-id="c2921-111">Die Schritte 4 bis 6 sind für die Installation in einer lokalen Formularbibliothek:</span><span class="sxs-lookup"><span data-stu-id="c2921-111">Steps 4 through 6 are for installation into a local form library:</span></span>
    
4. <span data-ttu-id="c2921-112">Kopieren Sie alle Dateien an der entsprechenden Stelle auf dem lokalen Datenträger, wenn die Installation in der lokalen Formularbibliothek auf dem Computer des Benutzers ist.</span><span class="sxs-lookup"><span data-stu-id="c2921-112">Copy all files to the appropriate place on the local disk, if installation is to the local form library on the user's workstation.</span></span> <span data-ttu-id="c2921-113">Bei Bedarf ändern Sie die Konfigurationsdatei Formular entsprechend der aktuellen Pfade der Komponenten.</span><span class="sxs-lookup"><span data-stu-id="c2921-113">If necessary, modify the form configuration file to reflect current paths of components.</span></span> <span data-ttu-id="c2921-114">Die Konfigurationsdatei Formular kann relative Pfade enthalten, die in diesem Fall kann dieser Schritt nicht erforderlich sein.</span><span class="sxs-lookup"><span data-stu-id="c2921-114">The form configuration file can contain relative paths, in which case this step may not be necessary.</span></span>
    
5. <span data-ttu-id="c2921-115">Führen Sie die entsprechenden OLE-Registrierung Schritte aus, um den Formular-Server installiert wird den Nachrichtentyp zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c2921-115">Complete the appropriate OLE registration steps to associate the message type with the form server being installed.</span></span>
    
6. <span data-ttu-id="c2921-116">Wenn das Formular in der lokalen Formularbibliothek installiert wurde, kopieren Sie des Formulars Symboldatei (ICO) und Konfigurationsdateien (cfg) in das Verzeichnis %WINDOWS%\FORMS\CONFIGS damit das Formular automatisch wiederhergestellt werden kann, falls die Formularbibliothek beschädigt oder gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="c2921-116">If the form was installed into the local form library, copy the form's icon (.ico) and configuration (.cfg) files into the %WINDOWS%\FORMS\CONFIGS directory so the form can be automatically restored in case the form library is corrupted or deleted.</span></span> <span data-ttu-id="c2921-117">Dieser Schritt ist das empfohlene jedoch nicht zwingend erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c2921-117">This step is recommended but not mandatory.</span></span>
    
> [!NOTE]
> <span data-ttu-id="c2921-118">Ersetzen die Schritte 1 und 2 mit einem Aufruf der Funktion [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) können Sie die Installation in einer lokalen Formularbibliothek vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="c2921-118">You can simplify installation to a local form library by replacing steps 1 and 2 with a call to the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c2921-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2921-119">See also</span></span>



[<span data-ttu-id="c2921-120">Entwickeln von MAPI-Formularservern</span><span class="sxs-lookup"><span data-stu-id="c2921-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

