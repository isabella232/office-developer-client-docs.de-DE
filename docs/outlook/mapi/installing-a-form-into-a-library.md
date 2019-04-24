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
ms.openlocfilehash: 08470a80153e42136922ae502252d83de0125512
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317234"
---
# <a name="installing-a-form-into-a-library"></a><span data-ttu-id="7428e-103">Installieren eines Formulars in einer Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7428e-103">Installing a Form into a Library</span></span>

  
  
<span data-ttu-id="7428e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7428e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7428e-105">Der standardmäßige MAPI-Formular-Manager, der mit dem Windows SDK bereitgestellt wird, bietet keine Benutzeroberfläche für die Installation von Formularen in den verschiedenen Formularbibliotheken.</span><span class="sxs-lookup"><span data-stu-id="7428e-105">The default MAPI form manager supplied with the Windows SDK does not provide a user interface for installing forms in the various form libraries.</span></span> <span data-ttu-id="7428e-106">Aus diesem Grund müssen Sie eine kleine Anwendung oder detaillierte Anweisungen erstellen, mit denen Benutzer das Formular installieren können.</span><span class="sxs-lookup"><span data-stu-id="7428e-106">Because of this, you will have to create a small application — or detailed set of instructions — that users can use to install the form.</span></span>
  
<span data-ttu-id="7428e-107">Wenn Sie eine Installationsanwendung implementieren, müssen die folgenden Aktionen ausgeführt werden, um ein Formular in der Tabelle mit den zugeordneten Inhalten eines Ordners zu installieren:</span><span class="sxs-lookup"><span data-stu-id="7428e-107">If you implement an installation application, the series of actions it must perform to install a form into a folder's associated contents table are as follows:</span></span>
  
1. <span data-ttu-id="7428e-108">Rufen Sie die [MAPIOpenFormMgr](mapiopenformmgr.md) -Funktion auf, um den Formular-Manager zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7428e-108">Call the [MAPIOpenFormMgr](mapiopenformmgr.md) function to open the form manager.</span></span> 
    
2. <span data-ttu-id="7428e-109">Verwenden Sie [IMAPIFormMgr:: OpenFormContainer](imapiformmgr-openformcontainer.md) oder [IMAPIFormMgr:: SelectFormContainer](imapiformmgr-selectformcontainer.md) -Methode, um den Zielcontainer für das Formular auszuwählen und zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7428e-109">Use [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) or [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to select and open the target container for the form.</span></span> 
    
3. <span data-ttu-id="7428e-110">Verwenden Sie die [IMAPIFormContainer:: InstallForm](imapiformcontainer-installform.md) -Funktion, um das Formular zu installieren.</span><span class="sxs-lookup"><span data-stu-id="7428e-110">Use the [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) function to install the form.</span></span> 
    
    <span data-ttu-id="7428e-111">Die Schritte 4 bis 6 sind für die Installation in einer lokalen Formularbibliothek erforderlich:</span><span class="sxs-lookup"><span data-stu-id="7428e-111">Steps 4 through 6 are for installation into a local form library:</span></span>
    
4. <span data-ttu-id="7428e-112">Kopieren Sie alle Dateien an den entsprechenden Speicherort auf dem lokalen Datenträger, wenn die Installation in der lokalen Formularbibliothek auf der Arbeitsstation des Benutzers erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7428e-112">Copy all files to the appropriate place on the local disk, if installation is to the local form library on the user's workstation.</span></span> <span data-ttu-id="7428e-113">Ändern Sie bei Bedarf die Formular Konfigurationsdatei entsprechend den aktuellen Pfaden von Komponenten.</span><span class="sxs-lookup"><span data-stu-id="7428e-113">If necessary, modify the form configuration file to reflect current paths of components.</span></span> <span data-ttu-id="7428e-114">Die Formular Konfigurationsdatei kann relative Pfade enthalten, in diesem Fall ist dieser Schritt möglicherweise nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7428e-114">The form configuration file can contain relative paths, in which case this step may not be necessary.</span></span>
    
5. <span data-ttu-id="7428e-115">Führen Sie die entsprechenden OLE-Registrierungsschritte aus, um den Nachrichtentyp dem installierten Formularserver zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="7428e-115">Complete the appropriate OLE registration steps to associate the message type with the form server being installed.</span></span>
    
6. <span data-ttu-id="7428e-116">Wenn das Formular in der lokalen Formularbibliothek installiert wurde, kopieren Sie das Formularsymbol (ICO) und die Konfigurationsdateien (. cfg) in das Verzeichnis%WINDOWS%\FORMS\CONFIGS, damit das Formular automatisch wiederhergestellt werden kann, falls die Formularbibliothek beschädigt oder gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="7428e-116">If the form was installed into the local form library, copy the form's icon (.ico) and configuration (.cfg) files into the %WINDOWS%\FORMS\CONFIGS directory so the form can be automatically restored in case the form library is corrupted or deleted.</span></span> <span data-ttu-id="7428e-117">Dieser Schritt wird empfohlen, aber nicht zwingend erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7428e-117">This step is recommended but not mandatory.</span></span>
    
> [!NOTE]
> <span data-ttu-id="7428e-118">Sie können die Installation in einer lokalen Formularbibliothek vereinfachen, indem Sie die Schritte 1 und 2 durch einen Aufruf der [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) -Funktion ersetzen.</span><span class="sxs-lookup"><span data-stu-id="7428e-118">You can simplify installation to a local form library by replacing steps 1 and 2 with a call to the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7428e-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7428e-119">See also</span></span>



[<span data-ttu-id="7428e-120">Entwickeln von MAPI-Formular Servern</span><span class="sxs-lookup"><span data-stu-id="7428e-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

