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
# <a name="databasedesignmasterid-property-dao"></a>Database.DesignMasterID Property (DAO)

**Betrifft**: Access 2013, Office 2013

Mit dieser Eigenschaft wird ein 16-Byte-Wert festgelegt oder zurückgegeben, der den Designmaster in einer Replikatgruppe eindeutig identifiziert (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . DesignMasterID

*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Legen Sie die **DesignMasterID**-Eigenschaft nur dann fest, wenn Sie den aktuellen Designmaster verschieben müssen. Wenn Sie diese Eigenschaft festlegen, wird ein bestimmtes Replikat der Replikatgruppe zum Designmaster.

> [!NOTE]
> [!HINWEIS] Erstellen Sie in einer Replikatgruppe niemals einen zweiten Designmaster. Das Vorhandensein eines zweiten Designmasters kann zu Datenverlusten führen.

Unter extremen Bedingungen, z. B. wenn der Designmaster gelöscht oder beschädigt ist, können Sie diese Eigenschaft auf das aktuelle Replikat festlegen. Wird diese Eigenschaft jedoch auf ein Replikat festgelegt, obwohl die Gruppe bereits einen anderen Designmaster enthält, kann das die Replikatgruppe in zwei unvereinbare Gruppen spalten und eine weitere Synchronisierung von Daten verhindern.

Wenn Sie ein Replikat zum neuen Designmaster der Gruppe machen möchten, synchronisieren Sie es mit allen Replikaten der Gruppe, bevor Sie die **DesignMasterID**-Eigenschaft im Replikat festlegen. Das Replikat muss im Exklusivmodus geöffnet sein, damit es zum Designmaster gemacht werden kann.

Falls Sie ein schreibgeschütztes Replikat zum Designmaster machen, wird der Schreibschutz aufgehoben. Der alte Designmaster behält ebenfalls den Lese-/Schreibzugriff.

Die Einstellung der  DesignMasterID-Eigenschaft wird in der Systemtabelle MSysRepInfo gespeichert.

## <a name="example"></a>Beispiel

Dieses Beispiel legt die **DesignMasterID**-Eigenschaft auf die Einstellung der **ReplicaID**-Eigenschaft einer anderen Datenbank fest und macht diese Datenbank zum Designmaster der Replikatgruppe. Der alte und der neue Designmaster werden zum Aktualisieren der Designänderung synchronisiert. Damit dieser Code funktioniert, müssen Sie einen Designmaster und ein Replikat erstellen, deren Namen und Pfade wie erforderlich einschließen und diesen Code in einer anderen Datenbank als der des alten oder neuen Designmasters ausführen.

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

