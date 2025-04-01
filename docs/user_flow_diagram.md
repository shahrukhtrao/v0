# Sample User Flow Diagram

Below is a sample user flow diagram illustrating the process of user registration and onboarding for a mobile application.

```mermaid
flowchart TD
    A[User Opens App] --> B{Has Account?}
    B -->|No| C[Sign Up Screen]
    B -->|Yes| D[Login Screen]
    
    C --> E[Enter Email]
    E --> F[Enter Password]
    F --> G[Create Profile]
    G --> H[Verify Email]
    H --> I[Onboarding Tutorial]
    
    D --> J[Enter Credentials]
    J --> K{Valid Credentials?}
    K -->|No| L[Error Message]
    L --> J
    
    K -->|Yes| M[Dashboard]
    I --> M
    
    M --> N{Complete Profile?}
    N -->|No| O[Profile Completion Prompt]
    O --> P[Edit Profile]
    P --> M
    
    N -->|Yes| Q[Full App Access]
    Q --> R[Explore Features]
    R --> S[Personalized Recommendations]
    
    style A fill:#b5e8ff,stroke:#0078d4
    style M fill:#d4ffd4,stroke:#00a36c
    style Q fill:#d4ffd4,stroke:#00a36c
    style L fill:#ffcccc,stroke:#e60000
```

## Alternative User Flow: Feature Discovery

Below is an alternative user flow focusing on feature discovery and engagement.

```mermaid
graph TD
    A[User Lands on Home] --> B[Featured Content]
    A --> C[Navigation Menu]
    
    B --> D[View Content Details]
    D --> E{Interested?}
    
    E -->|Yes| F[Save/Bookmark]
    E -->|No| G[Browse More Content]
    G --> B
    
    C --> H[Explore Categories]
    H --> I[Filter Options]
    I --> J[Category Results]
    J --> D
    
    C --> K[Search Feature]
    K --> L[Enter Search Terms]
    L --> M[Search Results]
    M --> D
    
    F --> N[Personalization Engine]
    N --> O[Recommended Content]
    O --> D
    
    D --> P[Share Content]
    P --> Q[Social Sharing Options]
    
    style A fill:#f9d5e5,stroke:#d64161
    style N fill:#eeeeee,stroke:#777777
    style O fill:#e1f7d5,stroke:#97c15c
```

## E-Commerce Purchase Flow

Here's a sample e-commerce user purchase flow.

```mermaid
sequenceDiagram
    participant U as User
    participant C as Catalog
    participant S as Search
    participant P as Product Page
    participant Cart as Shopping Cart
    participant CO as Checkout
    participant O as Order Confirmation
    
    U->>C: Browse Products
    U->>S: Search for Product
    S->>C: Display Results
    U->>P: Select Product
    P->>U: View Details
    
    U->>P: Add to Cart
    P->>Cart: Update Cart
    Cart->>U: Notify Added
    
    U->>Cart: Review Cart
    U->>Cart: Update Quantity
    U->>CO: Proceed to Checkout
    
    CO->>U: Request Shipping Info
    U->>CO: Enter Shipping Details
    CO->>U: Request Payment Info
    U->>CO: Enter Payment Details
    
    CO->>U: Show Order Summary
    U->>CO: Confirm Order
    CO->>O: Process Order
    O->>U: Show Order Confirmation
    O->>U: Send Confirmation Email
```

These diagrams can be visualized using any Mermaid-compatible viewer, including many GitHub repositories, Notion, VSCode with Mermaid extensions, or online editors like [Mermaid Live Editor](https://mermaid.live/).