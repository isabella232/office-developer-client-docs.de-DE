---
title: IFreeBusyData
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c9a80ad3-6311-fe07-b6f7-9fd63424753b
ms.openlocfilehash: cd9d4dffd83e1995319b0f0d661435fedb78f28c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393208"
---
# <a name="ifreebusydata"></a>IFreeBusyData

Für einen bestimmten Benutzer ruft ab und legt einen Zeitraum fest und gibt eine Schnittstelle zum Aufzählen Datenblöcke Frei/Gebucht-Informationen in diesem Zeitraum zurück.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Erbt:  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Bereitgestellt von:  <br/> |Frei/Gebucht-Anbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IFreeBusyData  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Placeholder1](ifreebusydata-placeholder1.md) <br/> | *Dieser Member ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
|[EnumBlocks](ifreebusydata-enumblocks.md) <br/> |Ruft eine Schnittstelle, die Datenblöcke Frei/Gebucht-Informationen für einen Benutzer in einen angegebenen Zeitraum auflistet.  <br/> |
|["Platzhalter2"](ifreebusydata-placeholder2.md) <br/> | *Dieser Member ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
|[Placeholder3](ifreebusydata-placeholder3.md) <br/> | *Dieser Member ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
|[Placeholder4](ifreebusydata-placeholder4.md) <br/> | *Dieser Member ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
|[Placeholder5](ifreebusydata-placeholder5.md) <br/> | *Dieser Member ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
|[SetFBRange](ifreebusydata-setfbrange.md) <br/> |Legt die Zeitspanne für eine Enumeration der Datenblöcke Frei/Gebucht-Informationen für einen Benutzer fest.  <br/> |
|[Placeholder6](ifreebusydata-placeholder6.md) <br/> | *Dieser Member ist ein Platzhalter und wird nicht unterstützt.*  <br/> |
|[GetFBPublishRange](ifreebusydata-getfbpublishrange.md) <br/> |Dient zum Abrufen eines vordefinierten Zeitraums für eine Enumeration der Datenblöcke Frei/Gebucht-Informationen für einen Benutzer.  <br/> |
   
## <a name="remarks"></a>Hinweise

Die meisten der Elemente in dieser Schnittstelle sind Platzhalter für die interne Verwendung von Outlook reserviert und kann geändert werden. Frei/Gebucht-Anbieter müssen implementieren sie nur als angegebenen, zurückgeben, dass nur die angegebenen Werte zurückgeben.
  
## <a name="see-also"></a>Siehe auch

- [Informationen zur Frei/Gebucht-API](about-the-free-busy-api.md)
- [Konstanten (Frei/Gebucht-API)](constants-free-busy-api.md)

