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
ms.openlocfilehash: 30b23b424b8c76f0681d0128348590c1558e81ec
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929384"
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
> <P>Achten Sie beim Festlegen eines Replikatfilters oder einer Replikatbeziehung darauf, dass Datensätze im Teilreplikat, die die Einschränkungskriterien nicht erfüllen, aus dem Teilreplikat entfernt werden, jedoch nicht aus dem vollständigen Replikat. Wenn Sie z. B. die ReplicaFilter-Eigenschaft des TableDef-Objekts der Tabelle Customers im Teilreplikat auf "Region = 'CA'" festlegen und dann die Datenbank neu auffüllen, werden alle Datensätze für Kunden in Kalifornien eingefügt bzw. aktualisiert. Wenn Sie dann die ReplicaFilter-Eigenschaft auf "Region = 'FL'" (Florida) festlegen und die Datenbank neu auffüllen, werden alle Datensätze der Region Kalifornien aus dem Teilreplikat  entfernt. Alle Datensätze der Kunden aus Florida aus dem vollständigen Replikat werden eingefügt. Aus dem vollständigen Replikat werden keine Datensätze gelöscht. Vor dem Festlegen der ReplicaFilter- oder PartialReplica-Eigenschaft sollte das Teilreplikat, in dem Sie diese Eigenschaften festlegen, mit dem vollständigen Replikat synchronisiert werden. Damit wird sichergestellt, dass ausstehende Änderungen im Teilreplikat in das vollständige Replikat aufgenommen werden, bevor Datensätze aus dem Teilreplikat entfernt werden.</P>


