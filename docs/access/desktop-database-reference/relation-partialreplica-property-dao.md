---
title: Relation.PartialReplica-Eigenschaft (DAO)
TOCTitle: PartialReplica Property
ms:assetid: 3cb15639-371e-06e3-e2ba-30466ce09a72
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192692(v=office.15)
ms:contentKeyID: 48544324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053557
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 11f8017c01cec9af2da26bedaf689d69554e554c
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998188"
---
# <a name="relationpartialreplica-property-dao"></a>Relation.PartialReplica-Eigenschaft (DAO)

**Betrifft**: Access 2013, Office 2013

Legt einen Wert für ein **Relation**-Objekt fest, der angibt, ob die Beziehung berücksichtigt werden soll, wenn ein Teilreplikat von einem vollständigen Replikat aufgefüllt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Datenbanken). **Boolean**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . PartialReplica

*Ausdruck* Ein Ausdruck, der ein **Relation** -Objekt zurückgibt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung bzw. der Rückgabewert ist ein boolescher Datentyp, der **True** ist, wenn die Beziehung während der Synchronisation erzwungen werden soll.

Diese Eigenschaft gestattet es Ihnen, Daten vom vollständigen Replikat basierend auf Beziehungen zwischen Tabellen auf das Teilreplikat zu replizieren. Sie können die PartialReplica-Eigenschaft verwenden, wenn die Einstellung der ReplicaFilter-Eigenschaft alleine nicht ausreicht, um festzulegen, welche Daten auf das Teilreplikat repliziert werden sollen. Beispiel: Sie haben eine Datenbank, in der die Tabelle Customers eine 1:n-Beziehung zur Tabelle Orders hat. Sie möchten ein Teilreplikat konfigurieren, bei der nur Bestellungen von Kunden aus der Region Kalifornien (CA) repliziert werden (anstelle aller Bestellungen). Es ist nicht möglich, die ReplicaFilter-Eigenschaft für die Tabelle Orders auf Region = 'CA' festzulegen, da sich das Feld Region in der Tabelle Customers befindet und nicht in der Tabelle Orders.

Um alle Bestellungen aus der Region Kalifornien (CA) zu replizieren, müssen Sie angeben, dass die Beziehung zwischen den Tabellen Orders und Customers während der Replikation aktiv sein soll. Nach der Erstellung eines Teilreplikats wird es mit den folgenden Schritten mit allen Bestellungen aus der Region Kalifornien aufgefüllt:

1.  Legen Sie die **ReplicaFilter** -Eigenschaft für das Kunden **TableDef** -Objekt zum "Region = 'CA'".

2.  Legen Sie den Wert der PartialReplica-Eigenschaft für das Relation-Objekt entsprechend der Beziehung zwischen Orders und Customers auf True fest.

3.  Rufen Sie die **PopulatePartial**-Methode auf.
    

> [!NOTE]
> Wenn Sie einen Replikatfilter oder Replikat Relation festlegen, achten Sie darauf, dass Datensätze aus dem Teilreplikat, die die Einschränkungskriterien erfüllen, nicht aus dem Teilreplikat, aber nicht aus dem vollständigen Replikat entfernt werden sollen. Angenommen, Sie die **ReplicaFilter** -Eigenschaft festlegen, auf die Kunden **TableDef** in dem Teilreplikat zu "Region = 'CA'" und Sie dann erneut die Datenbank aufzufüllen. Dies wird einfügen oder aktualisieren alle Datensätze für Kunden-basierte Kalifornien (CA). 
> 
> Wenn Sie dann die **ReplicaFilter** -Eigenschaft zum Zurücksetzen "Region = 'FL'" und die Datenbank wieder auffüllen, alle Kalifornien (CA) Region Datensätze aus dem Teilreplikat entfernt werden und alle Datensätze aus Florida-basierte Kunden aus dem vollständigen Replikat eingefügt werden soll. Es werden keine Datensätze aus dem vollständigen Replikat gelöscht werden. 
>
> Bevor Sie die **ReplicaFilter** - oder **PartialReplica** -Eigenschaft festlegen, ist es ratsam, synchronisieren das Teilreplikat, in dem Sie diese Eigenschaften mit dem vollständigen Replikat festlegen. Dadurch wird sichergestellt, dass mit dem vollständigen Replikat ausstehenden Änderungen aus dem Teilreplikat zusammengeführt wird, bevor alle Datensätze aus dem Teilreplikat entfernt werden.


