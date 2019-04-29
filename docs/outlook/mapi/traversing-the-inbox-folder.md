---
title: DurchLaufen des postEingangsOrdners
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e954cb2d8029a31e7f69daaa7e8ed55a7953ac02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406556"
---
# <a name="traversing-the-inbox-folder"></a><span data-ttu-id="b3e97-103">DurchLaufen des postEingangsOrdners</span><span class="sxs-lookup"><span data-stu-id="b3e97-103">Traversing the Inbox Folder</span></span>

  
  
<span data-ttu-id="b3e97-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3e97-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="b3e97-105">**So wechseln Sie alle Nachrichten im Posteingang**</span><span class="sxs-lookup"><span data-stu-id="b3e97-105">**To cycle through all of the messages in the Inbox**</span></span>
  
1. <span data-ttu-id="b3e97-106">Rufen Sie [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) auf, um den Eintragsbezeichner des Posteingangs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b3e97-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="b3e97-107">Rufen Sie **IMAPIFolder:: OpenEntry** auf, um den Posteingang zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b3e97-107">Call **IMAPIFolder::OpenEntry** to open the Inbox.</span></span> 
    
3. <span data-ttu-id="b3e97-108">Rufen Sie die [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontentable-Methode des Posteingangs auf, um die Tabelle Inhalt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b3e97-108">Call the Inbox's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to retrieve the contents table.</span></span> 
    
4. <span data-ttu-id="b3e97-109">Rufen Sie die [IMAPITable::](imapitable-setcolumns.md) SetColumns-Methode der Inhaltstabelle auf, um den Spaltensatz auf **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) und alle anderen Spalten einzuschränken, die Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="b3e97-109">Call the contents table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and any other columns you require.</span></span> 
    
5. <span data-ttu-id="b3e97-110">Rufen Sie [IMAPITable:: QueryRows](imapitable-queryrows.md) auf, um eine Gruppe von Zeilen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b3e97-110">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve a group of rows.</span></span> 
    
6. <span data-ttu-id="b3e97-111">Bis keine Zeilen mehr in der Tabelle Contents vorhanden sind:</span><span class="sxs-lookup"><span data-stu-id="b3e97-111">Until there are no longer any rows in the contents table:</span></span>
    
1. <span data-ttu-id="b3e97-112">Rufen Sie [IMsgStore:: OpenEntry](imsgstore-openentry.md) auf, um die durch den Eintragsbezeichner dargestellte Nachricht aus jeder Zeile zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b3e97-112">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the message represented by the entry identifier from each row.</span></span> 
    
2. <span data-ttu-id="b3e97-113">Weisen Sie den Parameter _lppUnk_ einem lokalen **IMessage** -Schnittstellenzeiger zu.</span><span class="sxs-lookup"><span data-stu-id="b3e97-113">Assign the  _lppUnk_ parameter to a local **IMessage** interface pointer.</span></span> 
    
3. <span data-ttu-id="b3e97-114">Arbeiten mit den Eigenschaften der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b3e97-114">Work with the properties of the message.</span></span>
    
4. <span data-ttu-id="b3e97-115">Lassen Sie den Zeiger, auf den durch den _lppUnk_ -Parameter zeigt.</span><span class="sxs-lookup"><span data-stu-id="b3e97-115">Release the pointer pointed to by the  _lppUnk_ parameter.</span></span> 
    
5. <span data-ttu-id="b3e97-116">Rufen Sie [IMAPITable:: QueryRows](imapitable-queryrows.md) auf, um die nächste Gruppe von Zeilen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b3e97-116">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the next group of rows.</span></span> 
    
7. <span data-ttu-id="b3e97-117">Geben Sie die Tabelle Contents frei.</span><span class="sxs-lookup"><span data-stu-id="b3e97-117">Release the contents table.</span></span>
    

