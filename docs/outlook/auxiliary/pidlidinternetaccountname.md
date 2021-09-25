---
title: PidLidInternetAccountName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 5acca047-ff2a-716c-8dd4-b676fce1a3cf
description: Gibt den Anzeigenamen des Kontos zurück, das die Nachricht übermittelt hat.
ms.openlocfilehash: d9ea49525d5941991eb62962191eed00df6ebdbf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580314"
---
# <a name="pidlidinternetaccountname"></a>PidLidInternetAccountName

Gibt den Anzeigenamen des Kontos zurück, das die Nachricht übermittelt hat.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidInetAcctName  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008580  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft sollte denselben Wert enthalten, der von der Account Management API-Eigenschaft [PROP_ACCT_NAME](prop_acct_name.md) für das Konto zurückgegeben wird, das die Nachricht übermittelt hat. 
  
Nachrichtenspeicheranbieter machen diese benannte Eigenschaft und [PidLidInternetAccountStamp verfügbar,](pidlidinternetaccountstamp.md) sodass die folgenden Aktionen ausgeführt werden: 
  
- Wenn ein Benutzer in einer E-Mail-Nachricht auf **"Allen antworten"** klickt, entfernt Outlook die E-Mail-Adresse, die dem Konto zugeordnet ist, und wird in der Nachricht mit einem Stempel aus der Empfängerliste der Antwort versehen. Dieses Verhalten tritt auf, es sei denn, diese E-Mail-Adresse ist der Absender der ursprünglichen Nachricht. 
    
- Standardmäßig sendet Outlook Antworten und weitergeleitete Nachrichten über das Konto, das mit der ursprünglichen Nachricht gestempelt ist.
    
In der Regel übermittelt der Outlook-Protokoll-Manager Nachrichten, und Outlook legt die Eigenschaften **PidLidInternetAccountName** und **PidLidInternetAccountStamp** so fest, dass das Konto angegeben wird, das die Nachricht übermittelt hat. Wenn ein Nachrichtenspeicher jedoch eng mit einem Transport gekoppelt ist, übermittelt der Outlook Protokoll-Manager keine Nachrichten, und Outlook diese Eigenschaften nicht festlegen können. In diesem Szenario ruft Outlook die [IMAPIProp::GetIDsFromNames-Funktion](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) auf. Wenn der Nachrichtenspeicheranbieter diese benannten Eigenschaften verfügbar machen möchte, sollte er **IMAPIProp::GetIDsFromNames** implementieren und Eigenschaftstags über den Ausgabeparameter  *lppPropTags*  zurückgeben. Outlook können dann die [IMAPIProp::GetProps-Methode](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) mithilfe dieser Eigenschaftentags aufrufen, und der Nachrichtenspeicheranbieter kann den Kontonamen und den Stempel des gewünschten Kontos zurückgeben. 
  
Zur Unterstützung dieser benannten Eigenschaften sollten Speicheranbieter erwarten, dass Outlook **IMAPIProp::GetIDsFromNames** verwenden, um das Eigenschaftstag für diese Eigenschaft abzurufen. Outlook gibt die folgenden Werte für die [MAPINAMEID-Struktur](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) an, die dieser benannten Eigenschaft entspricht, die als Teil des Arrays übergeben wird, auf das durch den Eingabeparameter *lppPropNames* von **IMAPIProp::GetIDsFromNames** verwiesen wird. 
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_ID  <br/> |
|Kind.lID:  <br/> |dispidInetAcctName  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)
- [Konstanten (Account Management API)](constants-account-management-api.md)
- [Kanonische PidLidInternetAccountName-Eigenschaft](https://msdn.microsoft.com/library/29bedadf-903d-419d-804d-dc8bd92b745d%28Office.15%29.aspx)

