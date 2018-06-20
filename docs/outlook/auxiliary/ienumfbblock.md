---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 536c19aa314db9fca39298536c12464e71a71407
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790970"
---
# <a name="ienumfbblock"></a>IEnumFBBlock

Unterstützt den Zugriff auf und das Aufzählen von Datenblöcke Frei/Gebucht-Informationen für einen Benutzer innerhalb eines Zeitraums.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Erbt:  <br/> |[IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Bereitgestellt von:  <br/> |Frei/Gebucht-Anbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |**IEnumFBBlock** <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Nächste](ienumfbblock-next.md) <br/> |Ruft die Anzahl der nächste angegebene Blöcke mit Frei/Gebucht-Daten in eine Enumeration.  <br/> |
|[Überspringen](ienumfbblock-skip.md) <br/> |Überspringt eine angegebene Anzahl von Blöcken des Frei/Gebucht-Daten.  <br/> |
|[Reset](ienumfbblock-reset.md) <br/> |Setzt den Enumerator durch Festlegen des Cursors an den Anfang zurück.  <br/> |
|[Clone](ienumfbblock-clone.md) <br/> |Erstellt eine Kopie der Enumerator, verwenden die gleichen zeitliche Beschränkung jedoch festlegen des Cursors an den Anfang des den Enumerator.  <br/> |
|[Einschränken](ienumfbblock-restrict.md) <br/> |Legt eine Beschränkung auf die Enumeration, die einen angegebenen Zeitraum.  <br/> |
   
## <a name="remarks"></a>Hinweise

Eine Enumeration enthält Frei/Gebucht-Blöcke mit Daten, die nicht rechtzeitig überlappen. Wenn sich überschneidenden Elemente in einem Kalender sind, verbindet Outlook diese Elemente um Frei/Gebucht-Blöcke übereinander in der angegebenen Reihenfolge der Priorität-Enumeration bilden: Abwesenheits, gebucht, mit Vorbehalt.
  
Ein Anbieter Frei/Gebucht-Informationen ruft diese Schnittstelle und die für einen Zeitraum für einen Benutzer über [IFreeBusyData](ifreebusydata.md)-Enumeration.
  
## <a name="see-also"></a>Siehe auch

- [Über die Frei/Gebucht-API](about-the-free-busy-api.md)  
- [Konstanten (Frei/Gebucht-API)](constants-free-busy-api.md)  
- [IFreeBusyData](ifreebusydata.md)

