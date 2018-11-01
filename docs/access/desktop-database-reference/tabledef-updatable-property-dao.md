---
title: TableDef.Updatable Property (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e4908699aaea69a001a1abd3761b78607ae2640a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869820"
---
# <a name="tabledefupdatable-property-dao"></a>TableDef.Updatable Property (DAO)


**Betrifft**: Access 2013, Office 2013

Gibt einen Wert zurück, der anzeigt, ob ein DAO-Objekt geändert werden kann. Schreibgeschützter **Boolean**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . Aktualisierbar

*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die **Updatable**-Eigenschaft für ein neu erstelltes **TableDef**-Objekt ist immer **True** und für ein verknüpftes **TableDef**-Objekt **False**. Ein neues **TableDef**-Objekt kann nur an eine Datenbank angefügt werden, für die der Benutzer Schreibberechtigung besitzt.

