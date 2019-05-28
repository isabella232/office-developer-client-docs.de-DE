---
title: MFCMAPI als ein Codebeispiel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d72c224db8b3ae4bb6fee3d34f73d9949cda6b8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356861"
---
# <a name="mfcmapi-as-a-code-sample"></a><span data-ttu-id="e30d6-103">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="e30d6-103">MFCMAPI as a code sample</span></span>
 
<span data-ttu-id="e30d6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e30d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e30d6-105">Das MfcMapi-Beispiel verwendet die Messaging-API, um über eine grafische Benutzeroberfläche Zugriff auf MAPI-Speicher bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e30d6-105">The MFCMAPI sample uses the Messaging API to provide access to MAPI stores through a graphical user interface.</span></span> <span data-ttu-id="e30d6-106">Nachdem Sie dieses Beispiel heruntergeladen haben, können Sie die Quelldateien verwenden, um Beispiel Anwendungsfälle für viele MAPI-Schnittstellen und Verweise zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="e30d6-106">After you download this sample, you can use the source files to examine example usage cases for many of the MAPI interfaces and references.</span></span> <span data-ttu-id="e30d6-107">Weitere Informationen finden Sie unter [MAPI-Schnittstellen](mapi-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="e30d6-107">For more information, see [MAPI Interfaces](mapi-interfaces.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e30d6-108">Plattformen</span><span class="sxs-lookup"><span data-stu-id="e30d6-108">Platforms:</span></span>  <br/> |<span data-ttu-id="e30d6-109">Zu Kompilier Microsoft Visual Studio 2008 für Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="e30d6-109">Microsoft Visual Studio 2008 to compile for Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
### <a name="to-download-mfcmapi"></a><span data-ttu-id="e30d6-110">So laden Sie MfcMapi herunter</span><span class="sxs-lookup"><span data-stu-id="e30d6-110">To download MFCMAPI</span></span>
  
1. <span data-ttu-id="e30d6-111">Klicken Sie auf der Seite [MfcMapi](https://codeplex.com/MFCMAPI) auf die Registerkarte **Quell Code** .</span><span class="sxs-lookup"><span data-stu-id="e30d6-111">On the [MFCMAPI](https://codeplex.com/MFCMAPI) page, click the **Source Code** tab.</span></span> 
    
2. <span data-ttu-id="e30d6-112">Klicken Sie unter **Recent Check-ins**auf **herunterladen** für den neuesten Build.</span><span class="sxs-lookup"><span data-stu-id="e30d6-112">Under **Recent Check-Ins**, click **Download** for the most recent build.</span></span> 
    
3. <span data-ttu-id="e30d6-113">Lesen Sie den Lizenzvertrag, und klicken Sie dann auf **Ich stimme**zu.</span><span class="sxs-lookup"><span data-stu-id="e30d6-113">Read the license agreement, and then click **I Agree**.</span></span>
    
4. <span data-ttu-id="e30d6-114">Klicken Sie im Dialogfeld **Dateidownload** auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="e30d6-114">In the **File Download** dialog box, click **Save**.</span></span> <span data-ttu-id="e30d6-115">Suchen Sie im Dialogfeld **Speichern** unter den Ordner, in dem Sie die Quelldateien speichern möchten, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="e30d6-115">In the **Save As** dialog box, locate the folder in which you want to save the source files, and then click **Save**.</span></span>
    
5. <span data-ttu-id="e30d6-116">Klicken Sie im Dialogfeld **Download abgeschlossen** auf **Ordner öffnen**.</span><span class="sxs-lookup"><span data-stu-id="e30d6-116">In the **Download Complete** dialog box, click **Open Folder**.</span></span> <span data-ttu-id="e30d6-117">Sie können auch auf **Schließen** klicken, um das Dialogfeld zu schließen und die gezippten Quelldateien in dem Ordner zu suchen, in dem Sie Sie gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="e30d6-117">You can also click **Close** to close the dialog box and locate the zipped source files in the folder that you saved them in.</span></span> 
    
6. <span data-ttu-id="e30d6-118">Klicken Sie mit der rechten Maustaste auf die **MfcMapi-Versions\<Nummer\>. zip-** Datei, und klicken Sie dann auf **Alle extrahieren**.</span><span class="sxs-lookup"><span data-stu-id="e30d6-118">Right-click the **MFCMAPI-\<version number\>.zip** file, and then click **Extract All**.</span></span> <span data-ttu-id="e30d6-119">Klicken Sie im daraufhin angezeigten Dialogfeld auf **extrahieren** , um die Dateien in den angezeigten Ordner zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="e30d6-119">In the dialog box that appears, click **Extract** to extract the files to the folder that is displayed.</span></span> <span data-ttu-id="e30d6-120">Sie können auch auf **Durchsuchen** klicken, um einen anderen Ordner auszuwählen oder zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e30d6-120">You can also click **Browse** to select or create a different folder.</span></span> 
    
7. <span data-ttu-id="e30d6-121">Führen Sie Visual Studio 2008 als Administrator aus.</span><span class="sxs-lookup"><span data-stu-id="e30d6-121">Run Visual Studio 2008 as an administrator.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="e30d6-122">Wenn auf Ihrem Computer Windows XP installiert ist, müssen Sie als Administrator angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="e30d6-122">If your computer is running Windows XP, you must be logged in as an administrator.</span></span> <span data-ttu-id="e30d6-123">Wenn auf Ihrem Computer Windows Vista ausgeführt wird, müssen Sie als Administrator angemeldet sein, und Sie müssen mit der rechten Maustaste auf das Visual Studio 2008 Symbol klicken und dann auf **als Administrator ausführen**klicken.</span><span class="sxs-lookup"><span data-stu-id="e30d6-123">If your computer is running Windows Vista, you must be logged in as an administrator and you must right-click the Visual Studio 2008 icon and then click **Run as administrator**.</span></span> 
  
8. <span data-ttu-id="e30d6-124">Klicken Sie in Visual Studio 2008 auf **Datei**, dann auf **Öffnen**, und klicken Sie dann auf **Projekt/Projektmappe**.</span><span class="sxs-lookup"><span data-stu-id="e30d6-124">In Visual Studio 2008, click **File**, point to **Open**, and then click **Project/Solution**.</span></span>
    
9. <span data-ttu-id="e30d6-125">Wechseln Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, wählen Sie **MFCMapi. vcproj**aus, und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="e30d6-125">Browse to the location where you saved the sample, select **MFCMapi.vcproj**, and then click **Open**.</span></span>
    
10. <span data-ttu-id="e30d6-126">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="e30d6-126">On the **Build** menu, click **Build Solution**.</span></span>
    
11. <span data-ttu-id="e30d6-127">Klicken Sie im Dialogfeld **Datei speichern** unter auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="e30d6-127">In the **Save File As** dialog box, click **Save**.</span></span>
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a><span data-ttu-id="e30d6-128">So verwenden Sie MfcMapi als Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="e30d6-128">To use MFCMAPI as a code sample</span></span>
  
<span data-ttu-id="e30d6-129">Erweitern Sie im **Projektmappen-Explorer**das **MFCMapi** -Projekt, und überprüfen Sie die Dateien in den Knoten **Header Dateien**, **Ressourcendateien**und **Quelldateien** für Programmierszenarien.</span><span class="sxs-lookup"><span data-stu-id="e30d6-129">In **Solution Explorer**, expand the **MFCMapi** project and examine the files in the **Header Files**, **Resource Files**, and **Source Files** nodes for programming scenarios.</span></span> 
  
<span data-ttu-id="e30d6-130">Viele Methoden Themen im Abschnitt [MAPI-Schnittstellen](mapi-interfaces.md) zeigen auf MfcMapi-Quelldateien für Programmierbeispiele.</span><span class="sxs-lookup"><span data-stu-id="e30d6-130">Many method topics in the [MAPI Interfaces](mapi-interfaces.md) section point to MFCMAPI source files for programming examples.</span></span> <span data-ttu-id="e30d6-131">In [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) werden Sie beispielsweise angewiesen, die Funktion `CMsgStoreDlg::OnDisplayReceiveFolderTable` in der Datei MsgStoreDlg. cpp zu betrachten.</span><span class="sxs-lookup"><span data-stu-id="e30d6-131">For example, in [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) you are instructed to look at the function  `CMsgStoreDlg::OnDisplayReceiveFolderTable` in the MsgStoreDlg.cpp file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e30d6-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e30d6-132">See also</span></span>

- [<span data-ttu-id="e30d6-133">MAPI-Beispiele</span><span class="sxs-lookup"><span data-stu-id="e30d6-133">MAPI Samples</span></span>](mapi-samples.md)

