---
title: PidLidInternetAccountName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5acca047-ff2a-716c-8dd4-b676fce1a3cf
description: Gibt den Anzeigenamen des Kontos, das die Nachricht nicht übermittelt.
ms.openlocfilehash: 2bd27cc7f868fb3f255a002ed70d0cb9b79516e3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393537"
---
# <a name="pidlidinternetaccountname"></a>PidLidInternetAccountName

Gibt den Anzeigenamen des Kontos, das die Nachricht nicht übermittelt.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidInetAcctName  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Common  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008580  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Allgemeine messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft sollte den gleichen Wert enthalten, der von der Konto-Verwaltungs-API-Eigenschaft [PROP_ACCT_NAME](prop_acct_name.md) für das Konto zurückgegeben wird, die die Nachricht nicht übermittelt. 
  
Nachricht-Anbieter Bereitstellen dieser benannten Eigenschaft und [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md) , so dass folgende Aktionen ausgeführt werden: 
  
- Wenn ein Benutzer **auf alle Antworten** in einer e-Mail-Nachricht klickt, entfernt Outlook die e-Mail-Adresse, die das Konto zugeordnet ist und für die Nachricht aus der Empfängerliste der Antwort versehen ist. Dieses Verhalten tritt auf, es sei denn, diese e-Mail-Adresse der Absender der ursprünglichen Nachricht ist. 
    
- Standardmäßig wird Outlook sendet Antworten und weitergeleitete Nachrichten über das Konto auf die ursprüngliche Nachricht versehen ist.
    
In der Regel die Outlook-Protokollmanager Nachrichten übermittelt, und Outlook legt die Eigenschaften **PidLidInternetAccountName** und **PidLidInternetAccountStamp** , um das Konto anzugeben, das die Nachricht nicht übermittelt. Wenn ein Nachrichtenspeichers eng mit einer Transport verknüpft ist, die Outlook-Protokollmanager übermittelt keine Nachrichten und Outlook diese Eigenschaften kann nicht festgelegt werden. In diesem Szenario ruft Outlook die [IMAPIProp::GetIDsFromNames](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) -Funktion. Wenn der Nachricht Speicheranbieter diese benannten Eigenschaften verfügbar zu machen möchte, muss **IMAPIProp::GetIDsFromNames** implementieren und Eigenschaftentags über die Ausgabe Parameter *LppPropTags* zurückzugeben. Outlook kann mithilfe dieser Eigenschaftentags dann die [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) -Methode aufrufen, und der Nachricht Speicheranbieter den Kontonamen und Zeitstempel für das gewünschte Konto zurückgeben. 
  
Zur Unterstützung der folgende benannten Eigenschaften erwarten Anbieter Outlook **IMAPIProp::GetIDsFromNames** verwendet, um das Eigenschafts-Tag für diese Eigenschaft abzurufen. Outlook gibt die folgenden Werte für die [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) -Struktur, die dieser benannten Eigenschaft entspricht, die als Teil des Arrays an, der input-Parameter *LppPropNames* des **IMAPIProp::GetIDsFromNames**auf zeigt übergeben wird. 
  
|||
|:-----|:-----|
|x LpGuid:  <br/> |PSETID_Common  <br/> |
|UlKind:  <br/> |MNID_ID  <br/> |
|Kind.lID:  <br/> |dispidInetAcctName  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)
- [Konstanten (Account Management API)](constants-account-management-api.md)
- [PidLidInternetAccountName (kanonische Eigenschaft)](https://msdn.microsoft.com/library/29bedadf-903d-419d-804d-dc8bd92b745d%28Office.15%29.aspx)

