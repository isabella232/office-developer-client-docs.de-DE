---
title: PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 52003a4e-1b61-2965-5204-6601652dd15b
description: Gibt den Kontostempel des Kontos zurück, das die Nachricht übermittelt hat.
ms.openlocfilehash: c5da45268cefbe09588fdcfcda32e4e7a4be9d5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327727"
---
# <a name="pidlidinternetaccountstamp"></a><span data-ttu-id="f439a-103">PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="f439a-103">PidLidInternetAccountStamp</span></span>

<span data-ttu-id="f439a-104">Gibt den Kontostempel des Kontos zurück, das die Nachricht übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="f439a-104">Returns the account stamp of the account that delivered the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f439a-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="f439a-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f439a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f439a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f439a-107">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="f439a-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="f439a-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="f439a-108">Property set:</span></span>  <br/> |<span data-ttu-id="f439a-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="f439a-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="f439a-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="f439a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f439a-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="f439a-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="f439a-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f439a-112">Data type:</span></span>  <br/> |<span data-ttu-id="f439a-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f439a-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f439a-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f439a-114">Area:</span></span>  <br/> |<span data-ttu-id="f439a-115">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="f439a-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f439a-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f439a-116">Remarks</span></span>

<span data-ttu-id="f439a-117">Diese Eigenschaft sollte denselben Wert enthalten, der von der Account Management-API-Eigenschaft [PROP_ACCT_STAMP](prop_acct_stamp.md) für das Konto zurückgegeben wird, das die Nachricht übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="f439a-117">This property should contain the same value that is returned from the Account Management API property [PROP_ACCT_STAMP](prop_acct_stamp.md) for the account that delivered the message.</span></span> 
  
<span data-ttu-id="f439a-118">Nachrichtenspeicheranbieter machen diese benannte Eigenschaft und [PidLidInternetAccountName](pidlidinternetaccountname.md) verfügbar, sodass die folgenden Aktionen auftreten:</span><span class="sxs-lookup"><span data-stu-id="f439a-118">Message store providers expose this named property and [PidLidInternetAccountName](pidlidinternetaccountname.md) so that the following actions occur:</span></span> 
  
- <span data-ttu-id="f439a-119">Wenn ein Benutzer **in** einer E-Mail auf Alle antworten klickt, entfernt Outlook die E-Mail-Adresse, die dem Konto zugeordnet ist, und wird in der Nachricht aus der Empfängerliste der Antwort gestempelt.</span><span class="sxs-lookup"><span data-stu-id="f439a-119">When a user clicks **Reply to All** in an email message, Outlook removes the email address that is associated with the account and is stamped on the message from the recipient list of the reply.</span></span> <span data-ttu-id="f439a-120">Dieses Verhalten tritt auf, es sei denn, diese E-Mail-Adresse ist der Absender der ursprünglichen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="f439a-120">This behavior occurs unless this email address is the sender of the original message.</span></span> 
    
- <span data-ttu-id="f439a-121">Standardmäßig sendet Outlook Antworten und weitergeleitete Nachrichten über das Konto, das in der ursprünglichen Nachricht gestempelt ist.</span><span class="sxs-lookup"><span data-stu-id="f439a-121">By default, Outlook sends replies and forwarded messages through the account that is stamped on the original message.</span></span>
    
<span data-ttu-id="f439a-122">Normalerweise stellt der Outlook-Protokoll-Manager Nachrichten zu, und Outlook legt die **Eigenschaften PidLidInternetAccountName** und **PidLidInternetAccountStamp** fest, um das Konto anzugeben, das die Nachricht übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="f439a-122">Usually, the Outlook Protocol Manager delivers messages, and Outlook sets the **PidLidInternetAccountName** and **PidLidInternetAccountStamp** properties to indicate the account that delivered the message.</span></span> <span data-ttu-id="f439a-123">Wenn ein Nachrichtenspeicher jedoch eng mit einem Transport gekoppelt ist, liefert der Outlook-Protokoll-Manager keine Nachrichten, und Outlook eigenschaften können nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f439a-123">However, if a message store is tightly coupled with a transport, the Outlook Protocol Manager does not deliver messages and Outlook cannot set these properties.</span></span> <span data-ttu-id="f439a-124">In diesem Szenario wird Outlook [IMAPIProp::GetIDsFromNames-Funktion](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) aufruft.</span><span class="sxs-lookup"><span data-stu-id="f439a-124">In this scenario, Outlook calls the [IMAPIProp::GetIDsFromNames](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) function.</span></span> <span data-ttu-id="f439a-125">Wenn der Nachrichtenspeicheranbieter diese benannten Eigenschaften verfügbar machen möchte, sollte er **IMAPIProp::GetIDsFromNames** implementieren und Eigenschaftstags über den Ausgabeparameter *lppPropTags zurückgeben.*</span><span class="sxs-lookup"><span data-stu-id="f439a-125">If the message store provider wants to expose these named properties, it should implement **IMAPIProp::GetIDsFromNames** and return property tags through the output parameter  *lppPropTags*  .</span></span> <span data-ttu-id="f439a-126">Outlook können dann die [IMAPIProp::GetProps-Methode](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) mithilfe dieser Eigenschaftstags aufrufen, und der Nachrichtenspeicheranbieter kann den Kontonamen und den Stempel des gewünschten Kontos zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f439a-126">Outlook can then call the [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) method by using these property tags, and the message store provider can return the account name and stamp of the desired account.</span></span> 
  
<span data-ttu-id="f439a-127">Zur Unterstützung dieser benannten Eigenschaften sollten Speicheranbieter erwarten, dass Outlook **IMAPIProp::GetIDsFromNames** verwendet, um das Eigenschaftstag für diese Eigenschaft zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f439a-127">To support these named properties, store providers should expect Outlook to use **IMAPIProp::GetIDsFromNames** to obtain the property tag for this property.</span></span> <span data-ttu-id="f439a-128">Outlook gibt die folgenden Werte für die [MAPINAMEID-Struktur](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) an, die dieser benannten Eigenschaft entspricht, die als Teil des Arrays übergeben wird, auf das der Eingabeparameter *lppPropNames* von **IMAPIProp::GetIDsFromNames** verweist.</span><span class="sxs-lookup"><span data-stu-id="f439a-128">Outlook specifies the following values for the [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) structure that corresponds to this named property, which is passed as part of the array pointed at by the input parameter  *lppPropNames*  of **IMAPIProp::GetIDsFromNames**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f439a-129">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="f439a-129">lpGuid:</span></span>  <br/> |<span data-ttu-id="f439a-130">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="f439a-130">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="f439a-131">ulKind:</span><span class="sxs-lookup"><span data-stu-id="f439a-131">ulKind:</span></span>  <br/> |<span data-ttu-id="f439a-132">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="f439a-132">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="f439a-133">Kind.lID:</span><span class="sxs-lookup"><span data-stu-id="f439a-133">Kind.lID:</span></span>  <br/> |<span data-ttu-id="f439a-134">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="f439a-134">dispidInetAcctStamp</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f439a-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f439a-135">See also</span></span>

- [<span data-ttu-id="f439a-136">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="f439a-136">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="f439a-137">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="f439a-137">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="f439a-138">PidLidInternetAccountStamp (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f439a-138">PidLidInternetAccountStamp Canonical Property</span></span>](https://msdn.microsoft.com/library/819179fe-e58e-415c-abc7-1949036745ee%28Office.15%29.aspx)

