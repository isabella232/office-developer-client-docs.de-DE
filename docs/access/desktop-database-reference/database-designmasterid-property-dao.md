---
title: Database.DesignMasterID Property (DAO)
TOCTitle: DesignMasterID Property
ms:assetid: c0545561-d44f-5479-8ae0-e3955db91761
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822824(v=office.15)
ms:contentKeyID: 48547508
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053417
f1_categories:
- Office.Version=v15
ms.openlocfilehash: da9619102a955c9a7945d05e89a1e132371d2461
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868406"
---
# <a name="databasedesignmasterid-property-dao"></a><span data-ttu-id="91af6-102">Database.DesignMasterID Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="91af6-102">Database.DesignMasterID Property (DAO)</span></span>

<span data-ttu-id="91af6-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="91af6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="91af6-104">Mit dieser Eigenschaft wird ein 16-Byte-Wert festgelegt oder zurückgegeben, der den Designmaster in einer Replikatgruppe eindeutig identifiziert (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="91af6-104">Sets or returns a 16-byte value that uniquely identifies the Design Master in a replica set (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="91af6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="91af6-105">Syntax</span></span>

<span data-ttu-id="91af6-106">*Ausdruck* . DesignMasterID</span><span class="sxs-lookup"><span data-stu-id="91af6-106">*expression* .DesignMasterID</span></span>

<span data-ttu-id="91af6-107">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="91af6-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="91af6-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91af6-108">Remarks</span></span>

<span data-ttu-id="91af6-p101">Legen Sie die **DesignMasterID**-Eigenschaft nur dann fest, wenn Sie den aktuellen Designmaster verschieben müssen. Wenn Sie diese Eigenschaft festlegen, wird ein bestimmtes Replikat der Replikatgruppe zum Designmaster.</span><span class="sxs-lookup"><span data-stu-id="91af6-p101">You should set the **DesignMasterID** property only if you need to move the current Design Master. Setting this property makes a specific replica in the replica set the Design Master.</span></span>

> [!NOTE]
> <span data-ttu-id="91af6-p102">[!HINWEIS] Erstellen Sie in einer Replikatgruppe niemals einen zweiten Designmaster. Das Vorhandensein eines zweiten Designmasters kann zu Datenverlusten führen.</span><span class="sxs-lookup"><span data-stu-id="91af6-p102">Never create a second Design Master in a replica set. The existence of a second Design Master can result in the loss of data.</span></span>

<span data-ttu-id="91af6-p103">Unter extremen Bedingungen, z. B. wenn der Designmaster gelöscht oder beschädigt ist, können Sie diese Eigenschaft auf das aktuelle Replikat festlegen. Wird diese Eigenschaft jedoch auf ein Replikat festgelegt, obwohl die Gruppe bereits einen anderen Designmaster enthält, kann das die Replikatgruppe in zwei unvereinbare Gruppen spalten und eine weitere Synchronisierung von Daten verhindern.</span><span class="sxs-lookup"><span data-stu-id="91af6-p103">Under extreme circumstances— for example, if the Design Master is erased or corrupted— you can set this property at the current replica. However, setting this property at a replica when there is already another Design Master in the set might partition your replica set into two irreconcilable sets and prevent any further synchronization of data.</span></span>

<span data-ttu-id="91af6-p104">Wenn Sie ein Replikat zum neuen Designmaster der Gruppe machen möchten, synchronisieren Sie es mit allen Replikaten der Gruppe, bevor Sie die **DesignMasterID**-Eigenschaft im Replikat festlegen. Das Replikat muss im Exklusivmodus geöffnet sein, damit es zum Designmaster gemacht werden kann.</span><span class="sxs-lookup"><span data-stu-id="91af6-p104">If you decide to make a replica the new Design Master for the set, synchronize it with all the replicas in the replica set before setting the **DesignMasterID** property in the replica. The replica must be open in exclusive mode in order to make it the Design Master.</span></span>

<span data-ttu-id="91af6-117">Falls Sie ein schreibgeschütztes Replikat zum Designmaster machen, wird der Schreibschutz aufgehoben. Der alte Designmaster behält ebenfalls den Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="91af6-117">If you make a replica that is designated read-only into the Design Master, the target replica is made read/write; the old Design Master also remains read/write.</span></span>

<span data-ttu-id="91af6-118">Die Einstellung der  DesignMasterID-Eigenschaft wird in der Systemtabelle MSysRepInfo gespeichert.</span><span class="sxs-lookup"><span data-stu-id="91af6-118">The **DesignMasterID** property setting is stored in the MSysRepInfo system table.</span></span>

## <a name="example"></a><span data-ttu-id="91af6-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="91af6-119">Example</span></span>

<span data-ttu-id="91af6-p105">Dieses Beispiel legt die **DesignMasterID**-Eigenschaft auf die Einstellung der **ReplicaID**-Eigenschaft einer anderen Datenbank fest und macht diese Datenbank zum Designmaster der Replikatgruppe. Der alte und der neue Designmaster werden zum Aktualisieren der Designänderung synchronisiert. Damit dieser Code funktioniert, müssen Sie einen Designmaster und ein Replikat erstellen, deren Namen und Pfade wie erforderlich einschließen und diesen Code in einer anderen Datenbank als der des alten oder neuen Designmasters ausführen.</span><span class="sxs-lookup"><span data-stu-id="91af6-p105">This example sets the **DesignMasterID** property to the **ReplicaID** property setting of another database, making that database the Design Master in the replica set. The old and new Design Masters are synchronized to update the design change. For this code to work, you must create a Design Master and replica, include their names and paths as appropriate, and run this code from a database other than the old or new Design Master.</span></span>

```vb 
 Sub SetNewDesignMaster(strOldDM as String, _ 
    strNewDM as String) 
    
    Dim dbsOld As Database 
    Dim dbsNew As Database 
    
    ' Open the current Design Master in exclusive mode. 
    Set dbsOld = OpenDatabase(strOldDM, True) 
    
    ' Open the database that will become the new 
    ' Design Master. 
    Set dbsNew = OpenDatabase(strNewDM) 
    
    ' Make the new database the Design Master. 
    dbsOld.DesignMasterID = dbsNew.ReplicaID 
    
    ' Synchronize the old Design Master with the new 
    ' Design Master, and allow two-way exchanges. 
    dbsOld.Synchronize strNewDM, dbRepImpExpChanges 
    dbsOld.Close 
    dbsNew.Close 
 
 End Sub 
 
```

