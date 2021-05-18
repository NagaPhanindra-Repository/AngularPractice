# MCGiftCardManagementRepo
Spring boot Microservice and Angular App



------------------------------------------------------------------------
package com.codemer.cardholder.model;

import java.util.List;

public class AdministerPartiesRequest {
	 private RequestHeader requestHeader;
	    private String userCountry;
	    private String primaryPartyIndicator;
	    private String originalSourceSystem;
	    private List<Context> context ;
	    private List<Entity> entity ;

	    public RequestHeader getRequestHeader() {
	        return requestHeader;
	    }

	    public void setRequestHeader(RequestHeader requestHeader) {
	        this.requestHeader = requestHeader;
	    }

	    public String getUserCountry() {
	        return userCountry;
	    }

	    public void setUserCountry(String userCountry) {
	        this.userCountry = userCountry;
	    }

	    public String getPrimaryPartyIndicator() {
	        return primaryPartyIndicator;
	    }

	    public void setPrimaryPartyIndicator(String primaryPartyIndicator) {
	        this.primaryPartyIndicator = primaryPartyIndicator;
	    }

	    public String getOriginalSourceSystem() {
	        return originalSourceSystem;
	    }

	    public void setOriginalSourceSystem(String originalSourceSystem) {
	        this.originalSourceSystem = originalSourceSystem;
	    }

	    public List<Context> getContext() {
	        return context;
	    }

	    public void setContext(List<Context> context) {
	        this.context = context;
	    }

	    public List<Entity> getEntity() {
	        return entity;
	    }

	    public void setEntity(List<Entity> entity) {
	        this.entity = entity;
	    }

	    @Override
	    public String toString() {
	        StringBuilder sb = new StringBuilder();
	        sb.append(AdministerPartiesRequest.class.getName()).append('@').append(Integer.toHexString(System.identityHashCode(this))).append('[');
	        sb.append("requestHeader");
	        sb.append('=');
	        sb.append(((this.requestHeader == null)?"<null>":this.requestHeader));
	        sb.append(',');
	        sb.append("userCountry");
	        sb.append('=');
	        sb.append(((this.userCountry == null)?"<null>":this.userCountry));
	        sb.append(',');
	        sb.append("primaryPartyIndicator");
	        sb.append('=');
	        sb.append(((this.primaryPartyIndicator == null)?"<null>":this.primaryPartyIndicator));
	        sb.append(',');
	        sb.append("originalSourceSystem");
	        sb.append('=');
	        sb.append(((this.originalSourceSystem == null)?"<null>":this.originalSourceSystem));
	        sb.append(',');
	        sb.append("context");
	        sb.append('=');
	        sb.append(((this.context == null)?"<null>":this.context));
	        sb.append(',');
	        sb.append("entity");
	        sb.append('=');
	        sb.append(((this.entity == null)?"<null>":this.entity));
	        sb.append(',');
	        if (sb.charAt((sb.length()- 1)) == ',') {
	            sb.setCharAt((sb.length()- 1), ']');
	        } else {
	            sb.append(']');
	        }
	        return sb.toString();
	    }


}

  
  ---------------------------------------------------------------------------------
  
  
  package com.codemer.cardholder.model;

public class Context {
	 private String name;
	    private String externalReference;

	    public String getName() {
	        return name;
	    }

	    public void setName(String name) {
	        this.name = name;
	    }

	    public String getExternalReference() {
	        return externalReference;
	    }

	    public void setExternalReference(String externalReference) {
	        this.externalReference = externalReference;
	    }

	    @Override
	    public String toString() {
	        StringBuilder sb = new StringBuilder();
	        sb.append(Context.class.getName()).append('@').append(Integer.toHexString(System.identityHashCode(this))).append('[');
	        sb.append("name");
	        sb.append('=');
	        sb.append(((this.name == null)?"<null>":this.name));
	        sb.append(',');
	        sb.append("externalReference");
	        sb.append('=');
	        sb.append(((this.externalReference == null)?"<null>":this.externalReference));
	        sb.append(',');
	        if (sb.charAt((sb.length()- 1)) == ',') {
	            sb.setCharAt((sb.length()- 1), ']');
	        } else {
	            sb.append(']');
	        }
	        return sb.toString();
	    }

}

  
  
  ----------------------------------------------------------------------------
  
  
  package com.codemer.cardholder.model;

public class Entity {
	private String fullName;
    private PartiallyPopulatedPostalAddress partiallyPopulatedPostalAddress;

    public String getFullName() {
        return fullName;
    }

    public void setFullName(String fullName) {
        this.fullName = fullName;
    }

    public PartiallyPopulatedPostalAddress getPartiallyPopulatedPostalAddress() {
        return partiallyPopulatedPostalAddress;
    }

    public void setPartiallyPopulatedPostalAddress(PartiallyPopulatedPostalAddress partiallyPopulatedPostalAddress) {
        this.partiallyPopulatedPostalAddress = partiallyPopulatedPostalAddress;
    }

    @Override
    public String toString() {
        StringBuilder sb = new StringBuilder();
        sb.append(Entity.class.getName()).append('@').append(Integer.toHexString(System.identityHashCode(this))).append('[');
        sb.append("fullName");
        sb.append('=');
        sb.append(((this.fullName == null)?"<null>":this.fullName));
        sb.append(',');
        sb.append("partiallyPopulatedPostalAddress");
        sb.append('=');
        sb.append(((this.partiallyPopulatedPostalAddress == null)?"<null>":this.partiallyPopulatedPostalAddress));
        sb.append(',');
        if (sb.charAt((sb.length()- 1)) == ',') {
            sb.setCharAt((sb.length()- 1), ']');
        } else {
            sb.append(']');
        }
        return sb.toString();
    }

}

  
  ------------------------------------------------------------------------
  
  package com.codemer.cardholder.model;

public class PartiallyPopulatedPostalAddress {
	
	private String city;
    private String country;
    private String region;
    private String postalCode;
    private String addressLines1;
    private String addressLines2;

    public String getCity() {
        return city;
    }

    public void setCity(String city) {
        this.city = city;
    }

    public String getCountry() {
        return country;
    }

    public void setCountry(String country) {
        this.country = country;
    }

    public String getRegion() {
        return region;
    }

    public void setRegion(String region) {
        this.region = region;
    }

    public String getPostalCode() {
        return postalCode;
    }

    public void setPostalCode(String postalCode) {
        this.postalCode = postalCode;
    }

    public String getAddressLines1() {
        return addressLines1;
    }

    public void setAddressLines1(String addressLines1) {
        this.addressLines1 = addressLines1;
    }

    public String getAddressLines2() {
        return addressLines2;
    }

    public void setAddressLines2(String addressLines2) {
        this.addressLines2 = addressLines2;
    }

    @Override
    public String toString() {
        StringBuilder sb = new StringBuilder();
        sb.append(PartiallyPopulatedPostalAddress.class.getName()).append('@').append(Integer.toHexString(System.identityHashCode(this))).append('[');
        sb.append("city");
        sb.append('=');
        sb.append(((this.city == null)?"<null>":this.city));
        sb.append(',');
        sb.append("country");
        sb.append('=');
        sb.append(((this.country == null)?"<null>":this.country));
        sb.append(',');
        sb.append("region");
        sb.append('=');
        sb.append(((this.region == null)?"<null>":this.region));
        sb.append(',');
        sb.append("postalCode");
        sb.append('=');
        sb.append(((this.postalCode == null)?"<null>":this.postalCode));
        sb.append(',');
        sb.append("addressLines1");
        sb.append('=');
        sb.append(((this.addressLines1 == null)?"<null>":this.addressLines1));
        sb.append(',');
        sb.append("addressLines2");
        sb.append('=');
        sb.append(((this.addressLines2 == null)?"<null>":this.addressLines2));
        sb.append(',');
        if (sb.charAt((sb.length()- 1)) == ',') {
            sb.setCharAt((sb.length()- 1), ']');
        } else {
            sb.append(']');
        }
        return sb.toString();
    }

}

  
  -------------------------------------------------------------------------------------
  
  
  package com.codemer.cardholder.model;

public class RequestHeader {
	 private String userId;
	    private String systemName;
	    private String messageReference;

	    public String getUserId() {
	        return userId;
	    }

	    public void setUserId(String userId) {
	        this.userId = userId;
	    }

	    public String getSystemName() {
	        return systemName;
	    }

	    public void setSystemName(String systemName) {
	        this.systemName = systemName;
	    }

	    public String getMessageReference() {
	        return messageReference;
	    }

	    public void setMessageReference(String messageReference) {
	        this.messageReference = messageReference;
	    }

	    @Override
	    public String toString() {
	        StringBuilder sb = new StringBuilder();
	        sb.append(RequestHeader.class.getName()).append('@').append(Integer.toHexString(System.identityHashCode(this))).append('[');
	        sb.append("userId");
	        sb.append('=');
	        sb.append(((this.userId == null)?"<null>":this.userId));
	        sb.append(',');
	        sb.append("systemName");
	        sb.append('=');
	        sb.append(((this.systemName == null)?"<null>":this.systemName));
	        sb.append(',');
	        sb.append("messageReference");
	        sb.append('=');
	        sb.append(((this.messageReference == null)?"<null>":this.messageReference));
	        sb.append(',');
	        if (sb.charAt((sb.length()- 1)) == ',') {
	            sb.setCharAt((sb.length()- 1), ']');
	        } else {
	            sb.append(']');
	        }
	        return sb.toString();
	    }

}

  
  ----------------------------------------
  
  
  
  public AdministerPartiesRequest getAdminPartiesY() {
		AdministerPartiesRequest admin= new AdministerPartiesRequest();
		RequestHeader requestHeader=new RequestHeader();
		requestHeader.setUserId("NILOTPAL.DE");
		requestHeader.setSystemName("SubmissionHub");
		requestHeader.setMessageReference("3434434");
		admin.setRequestHeader(requestHeader);
		
		admin.setUserCountry("USA");
		admin.setPrimaryPartyIndicator("");
		admin.setOriginalSourceSystem("SubmissionHub");
		List contextList=new ArrayList();
		
		Context context=new Context();
		context.setName("SNCBYPASSFLG");
		context.setExternalReference("Y");
		contextList.add(context);
		admin.setContext(contextList);
		
		
		PartiallyPopulatedPostalAddress partialAdd=new PartiallyPopulatedPostalAddress();
		partialAdd.setCity("Schamburg");
		partialAdd.setCountry("USA");
		partialAdd.setPostalCode("60196");
		partialAdd.setRegion("IL");
		partialAdd.setAddressLines1("1299 Zurich Way");
		partialAdd.setAddressLines2("Address 1");
		
		Entity entity =new Entity();
		entity.setFullName("Mike Garage");
		entity.setPartiallyPopulatedPostalAddress(partialAdd);
		Entity entity2 =new Entity();
		entity2.setFullName("Ali Ayub");
		entity2.setPartiallyPopulatedPostalAddress(partialAdd);
		
		List entityList=new ArrayList();
		entityList.add(entity);
		entityList.add(entity2);
		
		admin.setEntity(entityList);
		
		return admin;
	}
