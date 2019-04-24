---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 2b37aa2000218acc0663ee8e2db12f01b93c0663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317626"
---
# <a name="ienumfbblock"></a>IEnumFBBlock

Unterstützt den Zugriff auf und das Aufzählen von Frei/Gebucht-Datenblöcken für einen Benutzer innerhalb eines Zeitintervalls.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Erbt von:  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Bereitgestellt von:  <br/> |Frei/Gebucht-Anbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |**IEnumFBBlock** <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Next](ienumfbblock-next.md) <br/> |Ruft die nächste angegebene Anzahl von Frei/Gebucht-Datenblöcken in einer Enumeration ab.  <br/> |
|[Skip](ienumfbblock-skip.md) <br/> |Überspringt eine angegebene Anzahl von Frei/Gebucht-Datenblöcken.  <br/> |
|[Reset](ienumfbblock-reset.md) <br/> |Setzt den Enumerator zurück, indem der Cursor auf den Anfang gesetzt wird.  <br/> |
|[Clone](ienumfbblock-clone.md) <br/> |Erstellt eine Kopie des Enumerators, wobei dieselbe Zeiteinschränkung verwendet wird, der Cursor jedoch auf den Anfang des Enumerators festgelegt wird.  <br/> |
|[Restrict](ienumfbblock-restrict.md) <br/> |Schränkt die Enumeration auf einen bestimmten Zeitraum ein.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Eine Aufzählung enthält frei/gebucht-Datenblöcke, die sich nicht rechtzeitig überlappen. Wenn sich überlappende Elemente in einem Kalender befinden, werden diese Elemente von Outlook zusammengeführt, um sich nicht überschneidende frei/gebucht-Blöcke in der Enumeration zu bilden, die auf dieser Rangfolge basieren: Abwesenheit, gebucht, mit Vorbehalt.
  
Ein frei/gebucht-Anbieter ruft diese Schnittstelle und die Enumeration für einen Zeitraum für einen Benutzer über [IFreeBusyData](ifreebusydata.md)ab.
  
## <a name="see-also"></a>Siehe auch

- [Über die Frei/Gebucht-API](about-the-free-busy-api.md)  
- [Konstanten (frei/gebucht-API)](constants-free-busy-api.md)  
- [IFreeBusyData](ifreebusydata.md)

