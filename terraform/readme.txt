# ------------------------------------------
# Terraform CLI Commands Cheat Sheet
# ------------------------------------------

# ------------------------------
# 1. Terraform Setup
# ------------------------------
terraform -version                 # Show Terraform version
terraform -help                    # Show help for commands

# ------------------------------
# 2. Initialize Working Directory
# ------------------------------
terraform init
# Downloads provider plugins and sets up the backend

# ------------------------------
# 3. Format and Validate Code
# ------------------------------
terraform fmt                      # Format *.tf files
terraform validate                 # Check syntax and schema of configuration

# ------------------------------
# 4. Plan Infrastructure Changes
# ------------------------------
terraform plan
# Shows what will be created/changed/destroyed

terraform plan -out=tfplan         # Save plan to a file

# ------------------------------
# 5. Apply Configuration
# ------------------------------
terraform apply
# Applies the changes (asks for confirmation)

terraform apply tfplan             # Apply previously saved plan file

# ------------------------------
# 6. Destroy Infrastructure
# ------------------------------
terraform destroy
# Destroys all resources created by Terraform

# ------------------------------
# 7. State Management
# ------------------------------
terraform show                     # Show current state
terraform state list               # List all resources in state
terraform state show <resource>    # Show detailed info of a resource

# ------------------------------
# 8. Output Values
# ------------------------------
terraform output                   # Show output variables
terraform output <name>            # Show specific output value

# ------------------------------
# 9. Providers & Modules
# ------------------------------
terraform providers                # Show providers in use
terraform get                      # Download modules
terraform init -upgrade            # Upgrade modules and providers

# ------------------------------
# 10. Environment Variables (Optional)
# ------------------------------
export TF_VAR_<variable_name>=<value>   # Set variables from environment
