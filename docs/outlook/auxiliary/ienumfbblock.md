---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 99c61a576061daec4ab6916bda1a62efe93dffd5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564596"
---
# <a name="ienumfbblock"></a>IEnumFBBlock

Unterstützt das Zugreifen auf und Aufzählen von Frei/Gebucht-Datenblöcken für einen Benutzer innerhalb eines Zeitraums.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Erbt von:  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Bereitgestellt von:  <br/> |Frei/Gebucht-Anbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |**IEnumFBBlock** <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Next](ienumfbblock-next.md) <br/> |Ruft die nächste angegebene Anzahl von Frei/Gebucht-Datenblöcken in einer Enumeration ab.  <br/> |
|[Skip](ienumfbblock-skip.md) <br/> |Überspringt eine angegebene Anzahl von Frei/Gebucht-Datenblöcken.  <br/> |
|[Reset](ienumfbblock-reset.md) <br/> |Setzt den Enumerator zurück, indem der Cursor auf den Anfang festgelegt wird.  <br/> |
|[Clone](ienumfbblock-clone.md) <br/> |Erstellt eine Kopie des Enumerators, wobei die gleiche Zeiteinschränkung verwendet wird, der Cursor jedoch auf den Anfang des Enumerators festgelegt wird.  <br/> |
|[Restrict](ienumfbblock-restrict.md) <br/> |Schränkt die Aufzählung auf einen angegebenen Zeitraum ein.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Eine Enumeration enthält Frei/Gebucht-Datenblöcke, die sich nicht in der Zeit überlappen. Wenn sich Elemente in einem Kalender überlappen, führt Outlook diese Elemente zu nicht überlappenden Frei/Gebucht-Blöcken in der Enumeration zusammen, basierend auf dieser Rangfolge: außer Haus, beschäftigt, mit Vorbehalt.
  
Ein Frei/Gebucht-Anbieter ruft diese Schnittstelle und die Enumeration für einen Zeitraum für einen Benutzer über [IFreeBusyData](ifreebusydata.md)ab.
  
## <a name="see-also"></a>Siehe auch

- [Informationen zur Frei/Gebucht-API](about-the-free-busy-api.md)  
- [Konstanten (Frei/Gebucht-API)](constants-free-busy-api.md)  
- [IFreeBusyData](ifreebusydata.md)

